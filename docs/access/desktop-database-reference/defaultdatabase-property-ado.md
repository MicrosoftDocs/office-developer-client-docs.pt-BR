---
<<<<<<< Título cabeça: propriedade DefaultDatabase (ADO) TOCTitle: propriedade DefaultDatabase (ADO) === título: a propriedade DefaultDatabase (ADO) TOCTitle: a propriedade DefaultDatabase (ADO)
>>>>>>> ms:assetid de mestre: a35c5631-f9d9-e51f-950b-e52169830d94 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249757(v=office.15) ms:contentKeyID: ms.date 48546784: 18/09/2015 mtps_version: v=office.15
---

<<<<<<< Cabeça
# <a name="defaultdatabase-property-ado"></a>Propriedade DefaultDatabase (ADO)
=======
# <a name="defaultdatabase-property-ado"></a>Propriedade DefaultDatabase (ADO)
>>>>>>> mestre


**Aplica-se a**: Access 2013 | Office 2013

Indica o banco de dados padrão para um objeto [Connection](connection-object-ado.md).

<<<<<<< Cabeça
## <a name="settings-and-return-values"></a>Configurações e valor de retorno
=======
## <a name="settings-and-return-values"></a>Configurações e valores de retorno
>>>>>>> mestre

Define ou retorna um valor **String** que avalia o nome de um banco de dados disponível no provedor.

## <a name="remarks"></a>Comentários

Use a propriedade **DefaultDatabase** para definir ou retornar o nome do banco de dados padrão em um objeto **Connection** específico.

Se houver um banco de dados padrão, as sequências SQL poderão usar uma sintaxe não qualificada para acessar objetos no banco de dados. Para acessar objetos em um banco de dados que não seja aquele especificado na propriedade **DefaultDatabase**, é preciso qualificar os nomes dos objetos com o nome do banco de dados desejado. Na conexão, o provedor gravará as informações do banco de dados padrão na propriedade **DefaultDatabase**. Alguns provedores permitem apenas um banco de dados por conexão, caso em que não é possível alterar a propriedade **DefaultDatabase**.

Algumas fontes de dados e provedores talvez não ofereçam suporte a esse recurso e podem retornar um erro ou uma cadeia de caracteres vazia.

**Uso de serviço de dados remotos** Essa propriedade não está disponível em um objeto de **Conexão** do cliente.

