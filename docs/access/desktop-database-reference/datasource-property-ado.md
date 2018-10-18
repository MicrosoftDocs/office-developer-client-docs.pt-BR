---
<<<<<<< Título cabeça: propriedade DataSource (ADO) TOCTitle: propriedade DataSource (ADO) === título: propriedade DataSource (ADO) TOCTitle: propriedade DataSource (ADO)
>>>>>>> ms:assetid de mestre: 5c5d6c9b-b7d4-45a5-0f6a-a5580a74361e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249325(v=office.15) ms:contentKeyID: ms.date 48545087: 18/09/2015 mtps_version: v=office.15
---

<<<<<<< Cabeça
# <a name="datasource-property-ado"></a>Propriedade DataSource (ADO)
=======
# <a name="datasource-property-ado"></a>Propriedade DataSource (ADO)
>>>>>>> mestre


**Aplica-se a**: Access 2013 | Office 2013

Indica um objeto que contém dados a serem representados como um objeto [Recordset](recordset-object-ado.md).

## <a name="remarks"></a>Comentários

Essa propriedade é usada para criar controles vinculados a dados no Ambiente de Dados. O Ambiente de Dados mantém as coleções de dados (fontes de dados) contendo objetos nomeados (*membros de dados*) que serão representados como um objeto **Recordset***.*

As propriedades [DataMember](datamember-property-ado.md) e **DataSource** devem ser usadas em conjunto.

O objeto referido deve implementar a interface **IDataSource** e deve conter uma interface **IRowset**.

**Uso**

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
