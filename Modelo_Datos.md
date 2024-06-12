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
client.json


