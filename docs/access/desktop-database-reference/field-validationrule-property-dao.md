---
title: Propriedade Field.ValidationRule (DAO)
TOCTitle: ValidationRule Property
ms:assetid: b07e644d-54d3-7199-6f99-178774e54398
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821784(v=office.15)
ms:contentKeyID: 48547123
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a737f19b33777ea9c3acaf3bc6a9de5144a4db6a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874073"
---
# <a name="fieldvalidationrule-property-dao"></a><span data-ttu-id="d2d42-102">Propriedade Field.ValidationRule (DAO)</span><span class="sxs-lookup"><span data-stu-id="d2d42-102">Field.ValidationRule Property (DAO)</span></span>


<span data-ttu-id="d2d42-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="d2d42-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d2d42-p101">Define ou retorna um valor que valida os dados em um campo à medida que estes são alterados ou adicionados a uma tabela (somente em espaços de trabalho do Microsoft Access). **String** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="d2d42-p101">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only). Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2d42-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2d42-106">Syntax</span></span>

<span data-ttu-id="d2d42-107">*expressão* . ValidationRule</span><span class="sxs-lookup"><span data-stu-id="d2d42-107">*expression* .ValidationRule</span></span>

<span data-ttu-id="d2d42-108">*expressão* Uma expressão que retorna um objeto **Field** .</span><span class="sxs-lookup"><span data-stu-id="d2d42-108">*expression* An expression that returns a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2d42-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2d42-109">Remarks</span></span>

<span data-ttu-id="d2d42-p102">As configurações ou os valores de retorno são um String que descreve uma comparação em um formulário de uma cláusula SQL WHERE sem a palavra reservada WHERE. Para um objeto ainda não acrescentado à coleção **[Fields](fields-collection-dao.md)**, essa propriedade será leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="d2d42-p102">The settings or return values is a String that describes a comparison in the form of an SQL WHERE clause without the WHERE reserved word. For an object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write.</span></span>

<span data-ttu-id="d2d42-p103">A propriedade **ValidationRule** determina se um campo contém ou não dados válidos. Se os dados não forem válidos, ocorrerá um erro interceptável de tempo de execução. A mensagem de erro retornado será o texto da propriedade **[ValidationText](field-validationtext-property-dao.md)**, se especificado, ou o texto da expressão especificada por **ValidationRule**.</span><span class="sxs-lookup"><span data-stu-id="d2d42-p103">The **ValidationRule** property determines whether or not a field contains valid data. If the data is not valid, a trappable run-time error occurs. The returned error message is the text of the **[ValidationText](field-validationtext-property-dao.md)** property, if specified, or the text of the expression specified by **ValidationRule**.</span></span>

<span data-ttu-id="d2d42-115">Para um objeto **[Field](field-object-dao.md)**, o uso da propriedade **ValidationRule** depende do objeto que contém a coleção **Fields** na qual o objeto **Field** foi acrescentado.</span><span class="sxs-lookup"><span data-stu-id="d2d42-115">For a **[Field](field-object-dao.md)** object, use of the **ValidationRule** property depends on the object that contains the **Fields** collection to which the **Field** object is appended.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d2d42-116">Objeto acrescentado a</span><span class="sxs-lookup"><span data-stu-id="d2d42-116">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="d2d42-117">Uso</span><span class="sxs-lookup"><span data-stu-id="d2d42-117">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d2d42-118"><strong>Índice</strong></span><span class="sxs-lookup"><span data-stu-id="d2d42-118"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="d2d42-119">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="d2d42-119">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2d42-120"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="d2d42-120"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="d2d42-121">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d2d42-121">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2d42-122"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="d2d42-122"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="d2d42-123">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d2d42-123">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2d42-124"><strong>Relação</strong></span><span class="sxs-lookup"><span data-stu-id="d2d42-124"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="d2d42-125">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="d2d42-125">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2d42-126"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="d2d42-126"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="d2d42-127">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d2d42-127">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d2d42-128">Somente há suporte para a validação em bancos de dados que usam o mecanismo do banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="d2d42-128">Validation is supported only for databases that use the Microsoft Access database engine.</span></span>

<span data-ttu-id="d2d42-p104">A expressão da cadeia de caracteres especificada pela propriedade **ValidationRule** de um objeto **Field** pode se referir apenas a esse **Field** e não às funções definidas pelo usuário, às funções agregadas SQL ou às consultas. Para definir uma propriedade **ValidationRule** do objeto **Field** quando a definição da propriedade **ValidateOnSet** for **True**, a expressão deverá analisar com sucesso o nome do campo (com o nome do campo como um operando implícito) e avaliá-lo como **True**. Caso a definição da propriedade **ValidateOnSet** seja **False**, a definição da propriedade **ValidationRule** será ignorada.</span><span class="sxs-lookup"><span data-stu-id="d2d42-p104">The string expression specified by the **ValidationRule** property of a **Field** object can refer only to that **Field**. The expression can't refer to user-defined functions, SQL aggregate functions, or queries. To set a **Field** object's **ValidationRule** property when its **ValidateOnSet** property setting is **True**, the expression must successfully parse (with the field name as an implied operand) and evaluate to **True**. If its **ValidateOnSet** property setting is **False**, the **ValidationRule** property setting is ignored.</span></span>


> [!NOTE]
> <P><span data-ttu-id="d2d42-133">Se você definir a propriedade como uma cadeia de caracteres concatenada com um valor não inteiro e os parâmetros do sistema especificarem um caractere decimal de fora dos EUA, como uma vírgula (por exemplo, strRule = "preço &gt; " &amp; lngPrice e lngPrice = 125,50), ocorrerá um erro quando seu código tenta validar todos os dados.</span><span class="sxs-lookup"><span data-stu-id="d2d42-133">If you set the property to a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strRule = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error will result when your code attempts to validate any data.</span></span> <span data-ttu-id="d2d42-134">Isso acontece porque durante a concatenação, o número será convertido para uma sequência que usa os caracteres decimais padrão do sistema e o mecanismo SQL do banco de dados do Microsoft Access aceita somente os caracteres decimais padrão dos EUA.</span><span class="sxs-lookup"><span data-stu-id="d2d42-134">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access database engine SQL only accepts U.S. decimal characters.</span></span></P>


