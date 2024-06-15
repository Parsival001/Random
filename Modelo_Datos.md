## Modelo de Datos
 **Client**
- `String` firstName
- `String` lastName
- `LocalDate` dateOfBirth
- `char` gender
- `String` address
- `String` phone
- `String` email
- `List<Policy>` policies
- `List<Price>` prices

 **Price**
- `Client` client
- `TypeOfPolicy` policyType
- `double` sumInsured
- `double` price

**Transaction**
- `String` transactionNumber
- `LocalDate` transactionDate
- `double` amount
- `Estado` state

**Policy**
- `String` policyNumber
- `LocalDate` issueDate
- `LocalDate` expirationDate
- `Estado` state
- `double` sumInsured
- `double` premium
- `List<Beneficiary>` beneficiaries
- `Payer payer`
- `Advisor` advisor
  
 **Payer**
- `String` firstName
- `String` lastName
- `String` address
- `String` phone
- `String` email
- `String` bankAccount

   **Notification**
- `TypeOfNotification` type
- `LocalDate` dateSent
- `String` channel
- `String` message

  **Beneficiary**
- `String` firstName
- `String` lastName
- `double` benefitPercentage
- `String` relationToInsured

  **Advisor**
- `String` firstName
- `String` lastName
- `String` id
- `String` phone
- `String` email
- `List<Client>` clients
- `List<Policy>` policies

## Estructura de Archivos XML/JSON ###
**clients.json**
\
\[\{"firstName" : "Leo",
\
  "LastName" : "Brune",
  \
  "dateOfBirth" : "dec 5, 2001",
  \
  'gender' : 'M',
  \
  "address" : "Las Maercedes",
  \
  "phone" : "0416-3407478",
  \
  "email" : "Leo_brune00@gmail.com",
  \
  "policies" : \[\{"625362718"}],
  \
  "prices" : \[\{"Client" : \[\{"Leo", "Brune","dec 5, 2001", 'M', "Las Maercedes", "0416-3407478","Leo_brune00@gmail.com"}], "Life Policy", price : 400 000}]

\
**Policies.json**
\
\[\{"policyNumber" : "625362718",
\
  "issueDate" : "dec 8, 2023",
  \
  "expirationDate" : "dec 8, 2043",
  \
  "state" : "PROCESSED",
  \
  sumInsured : 150 000,
  \
  premium : 200 000,
  \
  "beneficiaries" :\[\{"Brune", 100.00, "life insurance"}],
  \
  "payer" : \["Leo", "Brune", "Las Maercedes", "0416-3407478", "Leo_brune00@gmail.com", "029837829290"],
  \
  "advisor" : \[\"Maria", "Cruz", "mcruz.97", "0414-3456324", "mcruz.97@provid.og.ve", \[\{"Leo", "Brune","dec 5, 2001", 'M', "Las Maercedes", "04163407478","Leo_brune00@gmail.com"}], \[\{"625362718"}]]
  }]
\
**Payers.json**
\
\[\{"firstName" : "Leo",
\
  "LastName" : "Brune",
  \
  "address" : "Las Maercedes",
  \
  "phone" : "0416-3407478",
  \
  "email" : "Leo_brune00@gmail.com",
  \
  "bankAccount" :  "029837829290"
}]
\
**Beneficiaries.json**
\
\[\{"firstName" : "Leo",
  "LastName" : "Brune",
  benefitPercentage : 100.00,
  "relationToInsured" : "life insurance"
}]
\
**Advisors.json**
\
\[\{ "firstName" : "Maria",
\
   "LastName" : "Cruz",
   \
   "id" : "mcruz.97",
   \
   "phone" : "0414-3456324",
   \
   "email" : "mcruz.97@provid.og.ve",
   \
   "clients" : \[\{"Leo", "Brune","dec 5, 2001", 'M', "Las Maercedes", "0416-3407478","Leo_brune00@gmail.com"}],
   \
   "policies" : \[\{"625362718"}]
}]
\
**Prices.json**
\
\[\{ "Client" : \[\{"Leo", "Brune","dec 5, 2001", 'M', "Las Maercedes", "0416-3407478","Leo_brune00@gmail.com"}],
\
   "policyType" : "Life Policy",
   \
   sumInsured : 150,000,
   \
   price : 400 000
}]
\
**Transactions.json**
\
\[\{ "transactionNumber" : "732829101029",
\
   "transactionDate" : "dec 8, 2023",
   \
   amount : 400 000,
   \
   "state" : "PROCESSED",
\}\]
\
**Notifications.json**
\
\[\{"type" : EMAIL,
\
  "dateSent" : "dec 9, 2023",
  \
  "channel" : "mcruz.97@provid.og.ve",
  \
  "message" : "Good afternoon Mr. Brune, you're life insurance has been aproved"
}]


