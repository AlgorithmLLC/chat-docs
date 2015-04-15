### editedGroup object
```javascript
editedgroup = {
	// Обновленная группа
	"group":
	{
		"id":139,
		"avatar":"311d6400-14ae-4247-af7a-4269bbc64a00",
		"admin_id":12,
		"created_at":"2015-02-03 15:36:20",
		"updated_at":"2015-02-03 15:36:20",
		"created_by":12,
		"updated_by":12,
		"Recipients":
		{
			"12":{"id":12,"username":"10002","domain_id":1},
			"14":{"id":14,"username":"10004","domain_id":1,}
		},
		"Body":	{"id":204,"name":"XiBDRTDLV+U+vWOB2O41wH6MXAiFW2AQ1aTjnSPXawSG6uFx","group_id":139,"recipient_id":12,"nonce":"cyelfuh4QEuKQHuj1HA+bEqq9BaGG42a","key_id":211,"key_from_id":211,"created_at":"2015-02-03 15:36:20","updated_at":"2015-02-03 16:41:48"}
	},
	// Обновленные диалоги
	"dialogs":[
		{
			"id":444,
			"group_id":139,
			"created_at":"2015-02-03 15:36:20",
			"updated_at":"2015-02-03 15:36:20",
			"created_by":12,
			"updated_by":12,
			"Body":
			{
				"12":{"id":554,"name":"VIuTU7emOXiFE61zeAHu+/xt+lWmu4bvLSuLeqV7jm8=","dialog_id":444,"recipient_id":12,"nonce":"5sGXZcVWc8wbTQaZj388yVk4FhAhlsnF","key_id":211,"key_from_id":211,"created_at":"2015-02-03 15:36:20","updated_at":"2015-02-03 16:41:48"}
			},
			"Recipients":
			{
				"12":{"id":12},
				"14":{"id":14}
			}
		}
	],
	// Сообщения об обновлениях в группе
	"messages":[
		//Сообщение о добавленных пользователях
		{
			"id":6977,
			"dialog_id":444,
			"edited_at":null,
			"type":"service.group.user.invited",
			"created_at":"2015-02-03 16:41:48",
			"updated_at":"2015-02-03 16:41:48",
			"created_by":12,
			"updated_by":12,
			"Body":
			{
				"12":{"id":6270,"body":"3TcIv+ohyLDkiic7d9LbPKZu2NGf3HJzKBt0mwxNCngwYV2CaqLu2g57RJJ0HU3ZxHfZpza4/muB+Fu93z7NRg==","props":null,"read_date":"2015-02-03 16:41:48","is_received":false,"message_id":6977,"recipient_id":12,"nonce":"RJfCR0JB3+cE7LhebvfJJwIsRpD0Nue3","key_id":211,"key_from_id":211,"created_at":"2015-02-03 16:41:48","updated_at":"2015-02-03 16:41:48"}
			},
			"Attachments":[],
			"Creator":{"id":12,"username":"10002","domain_id":1}
		},
		// Сообшение о переименовании группы
		{
			"id":6976,
			"dialog_id":444,
			"edited_at":null,
			"type":"service.group.renamed",
			"created_at":"2015-02-03 16:41:48",
			"updated_at":"2015-02-03 16:41:48",
			"created_by":12,
			"updated_by":12,
			"Body":
			{
				"12":{"id":6268,"body":"lqfAuJgMErAxE4dC2c4WlyU1oVPQbvuEQZoDk3ZTKmCkLaZz/welef/3FfuS+eHIgh3CKTG/XixSNtkl40wNCQ0=","props":null,"read_date":"2015-02-03 16:41:48","is_received":false,"message_id":6976,"recipient_id":12,"nonce":"HcVlokFtZ3Y3MTqGRwt4qYFxt8t+bwTc","key_id":211,"key_from_id":211,"created_at":"2015-02-03 16:41:48","updated_at":"2015-02-03 16:41:48"}
			},
			"Attachments":[],
			"Creator":{"id":12,"username":"10002","domain_id":1}
		},
		// Сообщение об исключенных из группы
		{
			"id":6978,
			"dialog_id":444,
			"edited_at":null,
			"type":"service.group.user.kicked",
			"created_at":"2015-02-03 16:41:48",
			"updated_at":"2015-02-03 16:41:48",
			"created_by":12,
			"updated_by":12,
			"Body":
			{
				"12":{"id":6272,"body":"L5kpEIj5MVuusx7vPnhKBAcrQa8kHCznrHuouuC6LNCtqZ4SQVR8j6YRBNSpa+6J3JB4sdfsdffsPE8rL8nOF7r2","props":null,"read_date":"2015-02-03 16:41:48","is_received":false,"message_id":6978,"recipient_id":12,"nonce":"9Q7EWeTvYcWCfkiDaoCzxdNt2MuavfbZ","key_id":211,"key_from_id":211,"created_at":"2015-02-03 16:41:48","updated_at":"2015-02-03 16:41:48"}
			},
			"Attachments":[],
			"Creator":{"id":12,"username":"10002","domain_id":1}
		}
	]
}
```
