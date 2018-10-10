---
title: Propriedade Field2.ValidationRule (DAO)
TOCTitle: ValidationRule Property
ms:assetid: 5464d2de-f3d7-5d6b-4fc5-66df6a5540cb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194105(v=office.15)
ms:contentKeyID: 48544896
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bc2e2bee3a459c2f2b25b26bba4ca2fadd7fb945
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463083"
---
# <a name="field2validationrule-property-dao"></a><span data-ttu-id="ed84c-102">Propriedade Field2.ValidationRule (DAO)</span><span class="sxs-lookup"><span data-stu-id="ed84c-102">Field2.ValidationRule Property (DAO)</span></span>


<span data-ttu-id="ed84c-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ed84c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ed84c-p101">Define ou retorna um valor que valida os dados em um campo à medida que estes são alterados ou adicionados a uma tabela (somente em espaços de trabalho do Microsoft Access). **String** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="ed84c-p101">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only). Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed84c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ed84c-106">Syntax</span></span>

<span data-ttu-id="ed84c-107">*expressão* . ValidationRule</span><span class="sxs-lookup"><span data-stu-id="ed84c-107">*expression* .ValidationRule</span></span>

<span data-ttu-id="ed84c-108">*expressão* Uma expressão que retorna um objeto **Field2** .</span><span class="sxs-lookup"><span data-stu-id="ed84c-108">*expression* An expression that returns a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed84c-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed84c-109">Remarks</span></span>

<span data-ttu-id="ed84c-p102">As configurações ou os valores de retorno são uma String que descreve uma comparação em um formulário da cláusula SQL WHERE sem a palavra reservada WHERE. Para um objeto ainda não acrescentado à coleção **[Fields](fields-collection-dao.md)**, essa propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="ed84c-p102">The settings or return values is a String that describes a comparison in the form of an SQL WHERE clause without the WHERE reserved word. For an object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write.</span></span>

<span data-ttu-id="ed84c-p103">A propriedade **ValidationRule** determina se um campo contém ou não dados válidos. Se os dados não forem válidos, ocorrerá um erro de tempo de execução interceptável. A mensagem de erro retornada é o texto da propriedade **ValidationText**, se especificada, ou o texto da expressão especificada por **ValidationRule**.</span><span class="sxs-lookup"><span data-stu-id="ed84c-p103">The **ValidationRule** property determines whether or not a field contains valid data. If the data is not valid, a trappable run-time error occurs. The returned error message is the text of the **ValidationText** property, if specified, or the text of the expression specified by **ValidationRule**.</span></span>

<span data-ttu-id="ed84c-115">Para um objeto **Field2**, a utilização da propriedade **ValidationRule** depende do objeto que contém a coleção **Fields** à qual o objeto **Field2** foi acrescentado.</span><span class="sxs-lookup"><span data-stu-id="ed84c-115">For a **Field2** object, use of the **ValidationRule** property depends on the object that contains the **Fields** collection to which the **Field2** object is appended.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ed84c-116">Objeto acrescentado a</span><span class="sxs-lookup"><span data-stu-id="ed84c-116">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="ed84c-117">Uso</span><span class="sxs-lookup"><span data-stu-id="ed84c-117">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ed84c-118"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="ed84c-118"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="ed84c-119">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="ed84c-119">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed84c-120"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="ed84c-120"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="ed84c-121">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ed84c-121">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed84c-122"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="ed84c-122"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="ed84c-123">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ed84c-123">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed84c-124"><strong>Relação</strong></span><span class="sxs-lookup"><span data-stu-id="ed84c-124"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="ed84c-125">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="ed84c-125">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed84c-126"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="ed84c-126"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="ed84c-127">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ed84c-127">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ed84c-128">Somente há suporte para a validação em bancos de dados que usam o mecanismo do banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="ed84c-128">Validation is supported only for databases that use the Microsoft Access database engine.</span></span>

<span data-ttu-id="ed84c-p104">A expressão de sequência especificada pela propriedade **ValidationRule** de um objeto **Field2** pode se referir apenas a **Field2**. A expressão não pode se referir às funções definidas pelo usuário, às funções agregadas SQL nem às consultas. Para definir a propriedade **ValidationRule** de um objeto **Field2**, quando a configuração de sua propriedade **ValidateOnSet** for **True**, a expressão deve ser analisada com sucesso (com o nome do campo como um operando implícito) e avaliada como **True**. Se a configuração de sua propriedade **ValidateOnSet** for **False**, a configuração da propriedade **ValidationRule** será ignorada.</span><span class="sxs-lookup"><span data-stu-id="ed84c-p104">The string expression specified by the **ValidationRule** property of a **Field2** object can refer only to that **Field2**. The expression can't refer to user-defined functions, SQL aggregate functions, or queries. To set a **Field2** object's **ValidationRule** property when its **ValidateOnSet** property setting is **True**, the expression must successfully parse (with the field name as an implied operand) and evaluate to **True**. If its **ValidateOnSet** property setting is **False**, the **ValidationRule** property setting is ignored.</span></span>


> [!NOTE]
> <P><span data-ttu-id="ed84c-133">Se você definir a propriedade como uma cadeia de caracteres concatenada com um valor não inteiro e os parâmetros do sistema especificarem um caractere decimal de fora dos EUA, como uma vírgula (por exemplo, strRule = "preço &gt; " &amp; lngPrice e lngPrice = 125,50), ocorrerá um erro quando seu código tenta validar todos os dados.</span><span class="sxs-lookup"><span data-stu-id="ed84c-133">If you set the property to a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strRule = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error will result when your code attempts to validate any data.</span></span> <span data-ttu-id="ed84c-134">Isso acontece porque durante a concatenação, o número será convertido para uma sequência que usa os caracteres decimais padrão do sistema e o mecanismo SQL do banco de dados do Microsoft Access aceita somente os caracteres decimais padrão dos EUA.</span><span class="sxs-lookup"><span data-stu-id="ed84c-134">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access database engine SQL only accepts U.S. decimal characters.</span></span></P>


