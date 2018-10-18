---
title: Método TableDef.CreateField (DAO)
TOCTitle: CreateField Method
ms:assetid: a83d797f-ea42-4a07-dd9e-b254755f0891
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821396(v=office.15)
ms:contentKeyID: 48546897
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052971
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1fd66910a3630d8968f75c5a59bb535520419994
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606980"
---
# <a name="tabledefcreatefield-method-dao"></a>Método TableDef.CreateField (DAO)

**Aplica-se a:** Access 2013 | Office 2013

Cria um novo objeto **[Field](field-object-dao.md)** (espaços de trabalho do Microsoft Access apenas).

## <a name="syntax"></a>Sintaxe

*expressão* . CreateField (_**nome**_, _**tipo**_, _**tamanho**_)

*expressão* Uma variável que representa um objeto **TableDef** .

### <a name="parameters"></a>Parâmetros

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome</p></th>
<th><p>Obrigatório/Opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Name</p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Uma string que denomina exclusivamente o novo objeto <strong>Field</strong>. Consulte a propriedade <strong><a href="connection-name-property-dao.md">Name</a></strong> para obter detalhes sobre nomes válidos de <strong>Field</strong>.</p></td>
</tr>
<tr class="even">
<td><p>Type</p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Uma constante que determina o tipo de dados do novo objeto <strong>Field</strong>. Consulte a propriedade <strong><a href="field-type-property-dao.md">Type</a></strong> para obter os tipos de dados válidos.</p></td>
</tr>
<tr class="odd">
<td><p>Size</p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Um Inteiro que indica o tamanho máximo, em bytes, de um objeto <strong>Field</strong> que contém o texto. Consulte a propriedade <strong><a href="field-size-property-dao.md">Size</a></strong> para obter valores válidos de size. Esse argumento é ignorado para campos numéricos e com largura fixa.</p></td>
</tr>
</tbody>
</table>


<<<<<<< Cabeça
### <a name="return-value"></a>Valor retornado
=======
### <a name="return-value"></a>Valor de retorno
>>>>>>> mestre

Field

## <a name="remarks"></a>Comentários

Você pode usar o método **CreateField** para criar um novo campo, bem como especificar o nome, o tipo de dados e o tamanho do campo. Se omitir uma ou mais dessas partes opcionais quando usar **CreateField**, você poderá usar uma instrução de atribuição apropriada para definir ou redefinir a propriedade correspondente antes de acrescentar o novo objeto à coleção. Depois de acrescentar o novo objeto, você poderá alterar algumas, mas não todas as configurações de propriedade. Consulte os tópicos individuais de propriedade para obter mais informações.

O tipo e argumentos de tamanho se aplicam somente aos objetos de **campo** em um objeto **TableDef** . Esses argumentos são ignorados quando um objeto **Field** é associado com um objeto **Index** ou **Relation**.

Se Name fizer referência a um objeto que já é um membro da coleção, ocorrerá um erro de tempo de execução quando você usa o método **[Append](fields-append-method-dao.md)** .

Para remover um objeto **Field** de uma coleção **Fields**, use o método **[Delete](fields-delete-method-dao.md)** na coleção. Você não pode excluir um objeto **Field** de uma coleção **Fields** do objeto **TableDef** depois de criar um índice que faz referência ao campo.

**Link fornecidos pela** comunidade [UtterAccess](https://www.utteraccess.com) . UtterAccess é o fórum principal de wiki e a Ajuda do Microsoft Access.

- [Adição de um campo de hiperlink a uma tabela existente com DAO](https://www.utteraccess.com/wiki/index.php/adding_a_hyperlink_field_to_an_existing_table_with_dao)

## <a name="example"></a>Exemplo

O exemplo a seguir mostra como criar um campo calculado. O método CreateField cria um campo denominado **FullName**. A propriedade de expressão, em seguida, é definida como a expressão que calcula o valor do campo.

**Código de exemplo fornecido pela** [referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Sub CreateCalculatedField()
        Dim dbs As DAO.Database
        Dim tdf As DAO.TableDef
        Dim fld As DAO.Field2
        
        ' get the database
        Set dbs = CurrentDb()
        
        ' create the table
        Set tdf = dbs.CreateTableDef("tblContactsCalcField")
        
        ' create the fields: first name, last name
        tdf.Fields.Append tdf.CreateField("FirstName", dbText, 20)
        tdf.Fields.Append tdf.CreateField("LastName", dbText, 20)
        
        ' create the calculated field: full name
        Set fld = tdf.CreateField("FullName", dbText, 50)
        fld.Expression = "[FirstName] & "" "" & [LastName]"
        tdf.Fields.Append fld
        
        ' append the table and cleanup
        dbs.TableDefs.Append tdf
        
    Cleanup:
        Set fld = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
    End Sub
```

