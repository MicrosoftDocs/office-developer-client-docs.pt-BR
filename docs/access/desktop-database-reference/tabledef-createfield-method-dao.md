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
localization_priority: Priority
ms.openlocfilehash: 713f2530369a824a6d7204655ded4333f7fe2765
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710430"
---
# <a name="tabledefcreatefield-method-dao"></a><span data-ttu-id="061d1-102">Método TableDef.CreateField (DAO)</span><span class="sxs-lookup"><span data-stu-id="061d1-102">TableDef.CreateField method (DAO)</span></span>

<span data-ttu-id="061d1-103">**Aplica-se a:** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="061d1-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="061d1-104">Cria um novo objeto **[Field](field-object-dao.md)** (espaços de trabalho do Microsoft Access apenas).</span><span class="sxs-lookup"><span data-stu-id="061d1-104">Creates a new **[Field](field-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="061d1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="061d1-105">Syntax</span></span>

<span data-ttu-id="061d1-106">*expressão* . CreateField (_**nome**_, _**tipo**_, _**tamanho**_)</span><span class="sxs-lookup"><span data-stu-id="061d1-106">*expression* .CreateField(_**Name**_, _**Type**_, _**Size**_)</span></span>

<span data-ttu-id="061d1-107">*expressão* Uma variável que representa um objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="061d1-107">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="061d1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="061d1-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="061d1-109">Nome</span><span class="sxs-lookup"><span data-stu-id="061d1-109">Name</span></span></p></th>
<th><p><span data-ttu-id="061d1-110">Obrigatório/opcional</span><span class="sxs-lookup"><span data-stu-id="061d1-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="061d1-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="061d1-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="061d1-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="061d1-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="061d1-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="061d1-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="061d1-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="061d1-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="061d1-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="061d1-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="061d1-p101">Uma string que denomina exclusivamente o novo objeto <strong>Field</strong>. Consulte a propriedade <strong><a href="connection-name-property-dao.md">Name</a></strong> para obter detalhes sobre nomes válidos de <strong>Field</strong>.</span><span class="sxs-lookup"><span data-stu-id="061d1-p101">A String that uniquely names the new <strong>Field</strong> object. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for details on valid <strong>Field</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="061d1-118"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="061d1-118"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="061d1-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="061d1-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="061d1-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="061d1-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="061d1-p102">Uma constante que determina o tipo de dados do novo objeto <strong>Field</strong>. Consulte a propriedade <strong><a href="field-type-property-dao.md">Type</a></strong> para obter os tipos de dados válidos.</span><span class="sxs-lookup"><span data-stu-id="061d1-p102">A constant that determines the data type of the new <strong>Field</strong> object. See the <strong><a href="field-type-property-dao.md">Type</a></strong> property for valid data types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="061d1-123"><em>Size</em></span><span class="sxs-lookup"><span data-stu-id="061d1-123"><em>Size</em></span></span></p></td>
<td><p><span data-ttu-id="061d1-124">Opcional</span><span class="sxs-lookup"><span data-stu-id="061d1-124">Optional</span></span></p></td>
<td><p><span data-ttu-id="061d1-125"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="061d1-125"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="061d1-p103">Um Inteiro que indica o tamanho máximo, em bytes, de um objeto <strong>Field</strong> que contém o texto. Consulte a propriedade <strong><a href="field-size-property-dao.md">Size</a></strong> para obter valores válidos de size. Esse argumento é ignorado para campos numéricos e com largura fixa.</span><span class="sxs-lookup"><span data-stu-id="061d1-p103">An Integer that indicates the maximum size, in bytes, of a <strong>Field</strong> object that contains text. See the <strong><a href="field-size-property-dao.md">Size</a></strong> property for valid size values. This argument is ignored for numeric and fixed-width fields.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="061d1-129">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="061d1-129">Return value</span></span>

<span data-ttu-id="061d1-130">Field</span><span class="sxs-lookup"><span data-stu-id="061d1-130">Field</span></span>

## <a name="remarks"></a><span data-ttu-id="061d1-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="061d1-131">Remarks</span></span>

<span data-ttu-id="061d1-p104">Você pode usar o método **CreateField** para criar um novo campo, bem como especificar o nome, o tipo de dados e o tamanho do campo. Se omitir uma ou mais dessas partes opcionais quando usar **CreateField**, você poderá usar uma instrução de atribuição apropriada para definir ou redefinir a propriedade correspondente antes de acrescentar o novo objeto à coleção. Depois de acrescentar o novo objeto, você poderá alterar algumas, mas não todas as configurações de propriedade. Consulte os tópicos individuais de propriedade para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="061d1-p104">You can use the **CreateField** method to create a new field, as well as specify the name, data type, and size of the field. If you omit one or more of the optional parts when you use **CreateField**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the new object, you can alter some but not all of its property settings. See the individual property topics for more details.</span></span>

<span data-ttu-id="061d1-136">O tipo e argumentos de tamanho se aplicam somente aos objetos de **campo** em um objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="061d1-136">The type and Size arguments apply only to **Field** objects in a **TableDef** object.</span></span> <span data-ttu-id="061d1-137">Esses argumentos são ignorados quando um objeto **Field** é associado com um objeto **Index** ou **Relation**.</span><span class="sxs-lookup"><span data-stu-id="061d1-137">These arguments are ignored when a **Field** object is associated with an **Index** or **Relation** object.</span></span>

<span data-ttu-id="061d1-138">Se Name fizer referência a um objeto que já é um membro da coleção, ocorrerá um erro de tempo de execução quando você usa o método **[Append](fields-append-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="061d1-138">If Name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="061d1-p106">Para remover um objeto **Field** de uma coleção **Fields**, use o método **[Delete](fields-delete-method-dao.md)** na coleção. Você não pode excluir um objeto **Field** de uma coleção **Fields** do objeto **TableDef** depois de criar um índice que faz referência ao campo.</span><span class="sxs-lookup"><span data-stu-id="061d1-p106">To remove a **Field** object from a **Fields** collection, use the **[Delete](fields-delete-method-dao.md)** method on the collection. You can't delete a **Field** object from a **TableDef** object's **Fields** collection after you create an index that references the field.</span></span>

<span data-ttu-id="061d1-141">**Link fornecidos pela** comunidade [UtterAccess](https://www.utteraccess.com) .</span><span class="sxs-lookup"><span data-stu-id="061d1-141">**Link provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="061d1-142">UtterAccess é o fórum principal de wiki e de ajuda do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="061d1-142">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="061d1-143">Adição de um campo de hiperlink a uma tabela existente com DAO</span><span class="sxs-lookup"><span data-stu-id="061d1-143">Adding a hyperlink field to an existing table with DAO</span></span>](https://www.utteraccess.com/wiki/index.php/adding_a_hyperlink_field_to_an_existing_table_with_dao)

## <a name="example"></a><span data-ttu-id="061d1-144">Exemplo</span><span class="sxs-lookup"><span data-stu-id="061d1-144">Example</span></span>

<span data-ttu-id="061d1-145">O exemplo a seguir mostra como criar um campo calculado.</span><span class="sxs-lookup"><span data-stu-id="061d1-145">The following example shows how to create a calculated field.</span></span> <span data-ttu-id="061d1-146">O método CreateField cria um campo denominado **FullName**.</span><span class="sxs-lookup"><span data-stu-id="061d1-146">The CreateField method creates a field named **FullName**.</span></span> <span data-ttu-id="061d1-147">A propriedade de expressão, em seguida, é definida como a expressão que calcula o valor do campo.</span><span class="sxs-lookup"><span data-stu-id="061d1-147">The Expression property is then set to the expression that calculates the value of the field.</span></span>

<span data-ttu-id="061d1-148">**Código de exemplo fornecido pela** [referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="061d1-148">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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

