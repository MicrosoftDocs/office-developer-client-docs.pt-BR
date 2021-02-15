---
title: Propriedade Field2.ValidationRule (DAO)
TOCTitle: ValidationRule Property
ms:assetid: 5464d2de-f3d7-5d6b-4fc5-66df6a5540cb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194105(v=office.15)
ms:contentKeyID: 48544896
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b6e9e50148f4b87a957ff2317b1b39522d7d4e1c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292647"
---
# <a name="field2validationrule-property-dao"></a><span data-ttu-id="44bd9-102">Propriedade Field2.ValidationRule (DAO)</span><span class="sxs-lookup"><span data-stu-id="44bd9-102">Field2.ValidationRule property (DAO)</span></span>


<span data-ttu-id="44bd9-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="44bd9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="44bd9-p101">Define ou retorna um valor que valida os dados em um campo, conforme ele é alterado ou adicionado a uma tabela (apenas espaços de trabalho do Microsoft Access). **String** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="44bd9-p101">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only). Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="44bd9-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="44bd9-106">Syntax</span></span>

<span data-ttu-id="44bd9-107">*expressão* . ValidationRule</span><span class="sxs-lookup"><span data-stu-id="44bd9-107">*expression* .ValidationRule</span></span>

<span data-ttu-id="44bd9-108">*expressão* Uma expressão que retorna um **objeto Field2** .</span><span class="sxs-lookup"><span data-stu-id="44bd9-108">*expression* An expression that returns a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="44bd9-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="44bd9-109">Remarks</span></span>

<span data-ttu-id="44bd9-p102">As configurações ou os valores de retorno são uma String que descreve uma comparação em um formulário da cláusula SQL WHERE sem a palavra reservada WHERE. Para um objeto ainda não acrescentado à coleção **[Fields](fields-collection-dao.md)**, essa propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="44bd9-p102">The settings or return values is a String that describes a comparison in the form of an SQL WHERE clause without the WHERE reserved word. For an object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write.</span></span>

<span data-ttu-id="44bd9-p103">A propriedade **ValidationRule** determina se um campo contém ou não dados válidos. Se os dados não forem válidos, ocorrerá um erro de tempo de execução interceptável. A mensagem de erro retornada é o texto da propriedade **ValidationText**, se especificada, ou o texto da expressão especificada por **ValidationRule**.</span><span class="sxs-lookup"><span data-stu-id="44bd9-p103">The **ValidationRule** property determines whether or not a field contains valid data. If the data is not valid, a trappable run-time error occurs. The returned error message is the text of the **ValidationText** property, if specified, or the text of the expression specified by **ValidationRule**.</span></span>

<span data-ttu-id="44bd9-115">Para um objeto **Field2**, a utilização da propriedade **ValidationRule** depende do objeto que contém a coleção **Fields** à qual o objeto **Field2** foi acrescentado.</span><span class="sxs-lookup"><span data-stu-id="44bd9-115">For a **Field2** object, use of the **ValidationRule** property depends on the object that contains the **Fields** collection to which the **Field2** object is appended.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="44bd9-116">Objeto acrescentado a</span><span class="sxs-lookup"><span data-stu-id="44bd9-116">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="44bd9-117">Uso</span><span class="sxs-lookup"><span data-stu-id="44bd9-117">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="44bd9-118"><strong>Índice</strong></span><span class="sxs-lookup"><span data-stu-id="44bd9-118"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="44bd9-119">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="44bd9-119">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44bd9-120"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="44bd9-120"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="44bd9-121">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44bd9-121">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44bd9-122"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="44bd9-122"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="44bd9-123">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44bd9-123">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44bd9-124"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="44bd9-124"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="44bd9-125">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="44bd9-125">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44bd9-126"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="44bd9-126"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="44bd9-127">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="44bd9-127">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="44bd9-128">A validação é aceita somente para bancos de dados que utilizam o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="44bd9-128">Validation is supported only for databases that use the Microsoft Access database engine.</span></span>

<span data-ttu-id="44bd9-p104">A expressão de sequência especificada pela propriedade **ValidationRule** de um objeto **Field2** pode se referir apenas a **Field2**. A expressão não pode se referir às funções definidas pelo usuário, às funções agregadas SQL nem às consultas. Para definir a propriedade **ValidationRule** de um objeto **Field2**, quando a configuração de sua propriedade **ValidateOnSet** for **True**, a expressão deve ser analisada com sucesso (com o nome do campo como um operando implícito) e avaliada como **True**. Se a configuração de sua propriedade **ValidateOnSet** for **False**, a configuração da propriedade **ValidationRule** será ignorada.</span><span class="sxs-lookup"><span data-stu-id="44bd9-p104">The string expression specified by the **ValidationRule** property of a **Field2** object can refer only to that **Field2**. The expression can't refer to user-defined functions, SQL aggregate functions, or queries. To set a **Field2** object's **ValidationRule** property when its **ValidateOnSet** property setting is **True**, the expression must successfully parse (with the field name as an implied operand) and evaluate to **True**. If its **ValidateOnSet** property setting is **False**, the **ValidationRule** property setting is ignored.</span></span>


> [!NOTE]
> <span data-ttu-id="44bd9-133">Se você definir a propriedade como uma cadeia de caracteres concatenada com um valor não inteiro, e os parâmetros do sistema especificarem um valor não-americano. caractere decimal, como uma vírgula (por exemplo, strRule = "PRICE &gt; " &amp; lngPrice e lngPrice = 125,50), ocorrerá um erro quando seu código tentar validar quaisquer dados.</span><span class="sxs-lookup"><span data-stu-id="44bd9-133">If you set the property to a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strRule = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error will result when your code attempts to validate any data.</span></span> <span data-ttu-id="44bd9-134">Isso ocorre porque, durante a concatenação, o número é convertido para uma sequência utilizando o caractere decimal padrão do seu sistema, e o mecanismo de banco de dados do Microsoft Access SQL aceita apenas caracteres decimais EUA.</span><span class="sxs-lookup"><span data-stu-id="44bd9-134">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access database engine SQL only accepts U.S. decimal characters.</span></span>


