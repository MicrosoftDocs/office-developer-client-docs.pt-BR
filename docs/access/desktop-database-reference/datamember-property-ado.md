---
<<<<<<< Título cabeça: propriedade DataMember (ADO) TOCTitle: propriedade DataMember (ADO) === título: propriedade DataMember (ADO) TOCTitle: propriedade DataMember (ADO)
>>>>>>> ms:assetid de mestre: f89e1d42-7993-764b-4e8a-2f449903f792 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250263(v=office.15) ms:contentKeyID: ms.date 48548787: 18/09/2015 mtps_version: v=office.15
---

<<<<<<< Cabeça
# <a name="datamember-property-ado"></a>Propriedade DataMember (ADO)
=======
# <a name="datamember-property-ado"></a>Propriedade DataMember (ADO)
>>>>>>> mestre

**Aplica-se a**: Access 2013 | Office 2013

Indica o nome do membro de dados que será recuperado do objeto referido pela propriedade [DataSource](datasource-property-ado.md).

<<<<<<< Cabeça
## <a name="settings-and-return-values"></a>Configurações e valor de retorno
=======
## <a name="settings-and-return-values"></a>Configurações e valores de retorno
>>>>>>> mestre

Define ou retorna um valor **String**. O nome não diferencia maiúsculas e minúsculas.

## <a name="remarks"></a>Comentários

Essa propriedade é usada para criar controles vinculados a dados no Ambiente de Dados. O Ambiente de Dados mantém as coleções de dados (fontes de dados) contendo objetos nomeados (*membros de dados*) que serão representados como um objeto [Recordset](recordset-object-ado.md)*.*

As propriedades **DataMember** e **DataSource** devem ser usadas em conjunto.

A propriedade **DataMember** determina qual objeto especificado pela propriedade **DataSource** será representado como um objeto **Recordset**. O objeto **Recordset** deve ser fechado antes que essa propriedade seja definida. Ocorrerá um erro se a propriedade **DataMember** não for definida antes da propriedade **DataSource** ou se o nome do **DataMember** não for reconhecido pelo objeto especificado na propriedade **DataSource**.

**Uso**

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
