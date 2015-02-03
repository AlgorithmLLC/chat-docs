### edit group(editedGroupContainer, ack)
```javascript
editedGroupContainer = {
	"group":
	{
		"id":139,
		"recipients":[16,12], // список участнико группы с учетом добавленных и исключенных
		"added":[16],         // список добавленных пользователей
		"kicked":[14],        // список исключенных пользователей
		// Зашифрованное название группы для всех участников группы с учетом добавленных и исключенных в этом фрейме
		"bodies":[
			{
				"name":"1HGGcejKya+awMNcJiWCx9cQZnUHiaEXiWw5DZW5lXsY0w==",
				"nonce":"XzTXi6Y8fEeN5nlvshjKyRnA52vPFtO0",
				"recipient_id":12,
				"key_id":211,
				"key_from_id":211
			},
			{
				"name":"/5jC9Tu5zS2tOMkmwBLm30EGuPngWeR8j6S1PasZ2OtXug==",
				"nonce":"SJbc4OkAovU5SXwFnWEtnhksqoTlFgFp",
				"recipient_id":16,
				"key_id":254,
				"key_from_id":211
			}
		],
	},
	// При изменении числа участников группы нужно обновить зашифрованные контейнеры с названиями диалогов в этой группе
	// Для каждого диалога в группе необходимо перешифровать название с учетом нового списка участников группы
	// в данном примере для пользователей [12, 16]
	"dialogs":[
		{
			"id":444,
			"bodies":[
				{
					"dialog_id":444,
					"name":"Ou/BRE2U84xnbhyTwF0LLJdmdwnM/AhwANfRW7g7D8g=",
					"nonce":"aXNErPNBlAgVQ5Dl2a3Kiu8NAeYXlKlW",
					"recipient_id":12,
					"key_id":211,
					"key_from_id":211
				},
				{
					"dialog_id":444,
					"name":"IGL5kZkTmy5b7SxWg0Y/7LraMNgF53QYpR0VJkuN5pM=",
					"nonce":"E+tX1/MdjHiGGn223PK2tbhXTL7/5q3g",
					"recipient_id":16,
					"key_id":254,
					"key_from_id":211
				}
			],
			"recipients":[16,12]
		}
	],
	// Если изменилось название группы, то создается такой блок сообщения
	// Уведомляются участники группы с учетом добавленных и исключенных пользователей
	"messages":[
		{
			"message":
			{
				"dialog_id":444,
				"type":"service.group.renamed"
			},
			"bodies":[
				{
					"body":"f/McOFR7BZAgp0Iux2tg6Cml/4CITSnWmP", //Если старое название расшифровано то 'Группа переименована с ' + (old_name) + ' на ' + new_name. Иначе 'Группа переименована на ' + new_name
					"nonce":"FYEo2U9NKGMQy7XbNTNpHLOAu+TOjj0u",
					"recipient_id":12,
					"key_id":211,
					"key_from_id":211
				},
				{
					"body":"Rl5yChNn+swgxSDz3sq0CHBn+YH+aR10Ha", //Если старое название расшифровано то 'Группа переименована с ' + (old_name) + ' на ' + new_name. Иначе 'Группа переименована на ' + new_name
					"nonce":"5jWJ4sFao9v9H/FsqPX/+sVd9wCkrlpN",
					"recipient_id":16,
					"key_id":254,
					"key_from_id":211
				}
			],
			"as_read":true,
			"attachments":[]
		},
		// Для каждого добавленного в группу пользователя создается такой блок сообщения
		// в блоке сообщения есть body для добавленного пользователя
		// body для каждого пользователя, кто остался в группе.
		// Исключенных в этом фрейме уведомлять о добавлении не нужно.
		{
			"message":
			{
				"dialog_id":444,
				"type":"service.group.user.invited"
			},
			"bodies":[
				{
					"body":"CjXeaD31jU1hp+879vzuPYbHthUHjm5jnr", // added_user.first_name + ' ' + added_user.last_name + ' добавлен в группу'
					"nonce":"X4UZmylI3a91BW3lVRu2Z3lBPWlEcoz9",
					"recipient_id":12,
					"key_id":211,
					"key_from_id":211
				},
				{
					"body":"7rb8a+2QKtRrP3lowPSBBLPp0RV3Qbq6fe", // 'Вы были добавлены в группу'
					"nonce":"4OiAXS8H1h2m7ltHdeG+kjp+su+xVxOS",
					"recipient_id":16,
					"key_id":254,
					"key_from_id":211
				}
			],
			"as_read":true,
			"attachments":[]
		},
		// Для каждого исключенного из группы пользователя создается такой блок сообщения
		// в блоке сообщения есть body для исключенного пользователя
		// body для каждого пользователя, кто сейчас в группе, с учетом добавленных
		{
			"message":
			{
				"dialog_id":444,
				"type":"service.group.user.kicked"
			},
			"bodies":[
				{
					"body":"b0W8y3TpGeanfFt+cVe0mD7qUqbq+5GCKUN", // kicked_user.first_name + ' ' + kicked_user.last_name + ' исключен из группы'
					"nonce":"CEi2GnhQyE8dteokBiXtwJNnVXLxD6he",
					"recipient_id":12,
					"key_id":211,
					"key_from_id":211
				},
				{
					"body":"noFTXg4OhQgqZkNODYxnMUsnxPkk0XTOLNT", // kicked_user.first_name + ' ' + kicked_user.last_name + ' исключен из группы'
					"nonce":"IqWWGtv6dtdCtu2kRrnkbuUvj4wPs9tL",
					"recipient_id":16,
					"key_id":254,
					"key_from_id":211
				},
				{
					"body":"O9b49TLNk0CROmpQyGFhLDN/zWiTYuLulVYz", // 'Вы были исключены из группы'
					"nonce":"8kLQBhJWZikKeplsgHlCYm6g3qCWk2kA",
					"recipient_id":14,
					"key_id":330,
					"key_from_id":211
				}
			],
			"as_read":true,
			"attachments":[]
		}
	]
}
```
Updates group.

Error types:
  - `something went wrong`

Returns `editedGroup object`.
```
editedGroup = {
  group: {...},
  dialogs: {...}
  messages: {...}
}
```

### important notice
