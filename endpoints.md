## Endpoints

###ACH Debit

	ach_debits
	- id
	- bank_account
	- amount
	- status


### Bank Account

	bank_accounts
	- id
	- name
	- account_number
	- routing_number
	- type
	

## Examples


`POST /ach_debits`

	{
		"bank_account": {
			"name": "Gottfried Leibniz",
			"account_number": "3819372930",
			"routing_number": "121042882",
			"type": "checking"
		}
		"amount": 1716,
	}

### pending

`GET /ach_debits/<ach_debits_id>`

	{
		"id": <ach_debit_id>,
		"bank_account": {
			"id": <bank_account_id>,
			"account_number": "xxxxxx2930",
			"routing_number": "121042882",
			"type": "checking"
		}
		"amount": 1716,
		"status": "pending",
		"status_updated_at": 1345567104
	}

### completed

`GET /ach_debits/<ach_debits_id>`

	{
		"id": <ach_debit_id>,
		"bank_account": {
			"id": <bank_account_id>,
			"account_number": "xxxxxx2930",
			"routing_number": "121042882",
			"type": "checking"
		}
		"amount": 1716,
		"status": "available",
		"status_updated_at": 1345567104
	}

### rejected

`GET /ach_debits/<ach_debit_id>`

	{
		"id": <ach_debit_id>,
		"bank_account": {
			"id": <bank_account_id>,
			"account_number": "xxxxxx2930",
			"routing_number": "121042882",
			"type": "checking"
		}
		"amount": 1716,
		"status": "rejected",
		"status_updated_at": 1345567104
	}
