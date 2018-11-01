---
title: Propriedade Recordset.ValidationRule (DAO)
TOCTitle: ValidationRule Property
ms:assetid: c9250c13-18fe-1ff7-7846-7872c49a1e3b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823208(v=office.15)
ms:contentKeyID: 48547671
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b4a15be2a1ef3ea31b078afb287ffa1f48dd232d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885042"
---
# <a name="recordsetvalidationrule-property-dao"></a><span data-ttu-id="c23d3-102">Propriedade Recordset.ValidationRule (DAO)</span><span class="sxs-lookup"><span data-stu-id="c23d3-102">Recordset.ValidationRule Property (DAO)</span></span>


<span data-ttu-id="c23d3-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="c23d3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c23d3-104">Define ou retorna um valor que valida os dados em um campo à medida que estes são alterados ou adicionados a uma tabela (somente em espaços de trabalho do Microsoft Access). **String** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c23d3-104">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only).Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c23d3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c23d3-105">Syntax</span></span>

<span data-ttu-id="c23d3-106">*expressão* . ValidationRule</span><span class="sxs-lookup"><span data-stu-id="c23d3-106">*expression* .ValidationRule</span></span>

<span data-ttu-id="c23d3-107">*expressão* Uma variável que representa um objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="c23d3-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c23d3-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="c23d3-108">Remarks</span></span>

<span data-ttu-id="c23d3-p101">As configurações ou valores de retorno são um **String** que descreve uma comparação no formulário de uma cláusula SQL WHERE sem a palavra reservada WHERE. Para um objeto ainda não acrescentado à coleção **Fields**, essa propriedade será leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c23d3-p101">The settings or return values is a **String** that describes a comparison in the form of an SQL WHERE clause without the WHERE reserved word. For an object not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="c23d3-p102">A propriedade **ValidationRule** determina se um campo contém ou não dados válidos. Se os dados não forem válidos, ocorrerá um erro interceptável de tempo de execução. A mensagem de erro retornada será o texto da propriedade **ValidationText**, se especificado, ou o texto da expressão especificada por **ValidationRule**.</span><span class="sxs-lookup"><span data-stu-id="c23d3-p102">The **ValidationRule** property determines whether or not a field contains valid data. If the data is not valid, a trappable run-time error occurs. The returned error message is the text of the **ValidationText** property, if specified, or the text of the expression specified by **ValidationRule**.</span></span>

<span data-ttu-id="c23d3-p103">Para um objeto **Recordset**, o uso da propriedade **ValidationRule** é somente leitura. Para um objeto **TableDef**, o uso da propriedade **ValidationRule** depende do status do objeto **TableDef**, como mostra a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c23d3-p103">For a **Recordset** object, use of the **ValidationRule** property is read-only. For a **TableDef** object, use of the **ValidationRule** property depends on the status of the **TableDef** object, as the following table shows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c23d3-116">TableDef</span><span class="sxs-lookup"><span data-stu-id="c23d3-116">TableDef</span></span></p></th>
<th><p><span data-ttu-id="c23d3-117">Uso</span><span class="sxs-lookup"><span data-stu-id="c23d3-117">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c23d3-118">Tabela base</span><span class="sxs-lookup"><span data-stu-id="c23d3-118">Base table</span></span></p></td>
<td><p><span data-ttu-id="c23d3-119">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c23d3-119">Read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c23d3-120">Tabela vinculada</span><span class="sxs-lookup"><span data-stu-id="c23d3-120">Linked table</span></span></p></td>
<td><p><span data-ttu-id="c23d3-121">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c23d3-121">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c23d3-122">Somente há suporte para a validação em bancos de dados que usam o mecanismo do banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="c23d3-122">Validation is supported only for databases that use the Microsoft Access database engine.</span></span>

<span data-ttu-id="c23d3-p104">A expressão da cadeia de caracteres especificada pela propriedade **ValidationRule** de um objeto **Field** pode se referir apenas a esse **Field** e não às funções definidas pelo usuário, às funções agregadas SQL ou às consultas. Para definir uma propriedade **ValidationRule** do objeto **Field** quando a definição da propriedade **ValidateOnSet** for **True**, a expressão deverá analisar com sucesso o nome do campo (com o nome do campo como um operando implícito) e avaliá-lo como **True**. Caso a definição da propriedade **ValidateOnSet** seja **False**, a definição da propriedade **ValidationRule** será ignorada.</span><span class="sxs-lookup"><span data-stu-id="c23d3-p104">The string expression specified by the **ValidationRule** property of a **Field** object can refer only to that **Field**. The expression can't refer to user-defined functions, SQL aggregate functions, or queries. To set a **Field** object's **ValidationRule** property when its **ValidateOnSet** property setting is **True**, the expression must successfully parse (with the field name as an implied operand) and evaluate to **True**. If its **ValidateOnSet** property setting is **False**, the **ValidationRule** property setting is ignored.</span></span>

<span data-ttu-id="c23d3-p105">A propriedade **ValidationRule** de um objeto **Recordset** ou **TableDef** pode se referir a vários campos desse objeto. As restrições observadas anteriormente neste tópico do objeto **Field** são aplicáveis.</span><span class="sxs-lookup"><span data-stu-id="c23d3-p105">The **ValidationRule** property of a **Recordset** or **TableDef** object can refer to multiple fields in that object. The restrictions noted earlier in this topic for the **Field** object apply.</span></span>

<span data-ttu-id="c23d3-129">Para um **Recordset** do tipo tabela, a propriedade **ValidationRule** herda a definição de propriedade de **ValidationRule** do objeto **TableDef** usado para criar o objeto **Recordset** do tipo tabela.</span><span class="sxs-lookup"><span data-stu-id="c23d3-129">For a table-type **Recordset** object, the **ValidationRule** property inherits the **ValidationRule** property setting of the **TableDef** object that you use to create the table-type **Recordset** object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="c23d3-130">Se você definir a propriedade como uma cadeia de caracteres concatenada com um valor não inteiro e os parâmetros do sistema especificarem um caractere decimal de fora dos EUA, como uma vírgula (por exemplo, strRule = "preço &gt; " &amp; lngPrice e lngPrice = 125,50), ocorrerá um erro quando seu código tenta validar todos os dados.</span><span class="sxs-lookup"><span data-stu-id="c23d3-130">If you set the property to a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strRule = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error will result when your code attempts to validate any data.</span></span> <span data-ttu-id="c23d3-131">Isso acontecerá porque durante a concatenação, o número será convertido em uma sequência que usa o caractere decimal padrão do sistema e o Microsoft Access SQL aceita somente os caracteres decimais do padrão dos EUA.</span><span class="sxs-lookup"><span data-stu-id="c23d3-131">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span></P>


