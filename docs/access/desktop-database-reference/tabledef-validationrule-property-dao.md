---
title: Propriedade TableDef.ValidationRule (DAO)
TOCTitle: ValidationRule Property
ms:assetid: 7dcd6f2c-45bc-a50b-727d-589371d5803f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196425(v=office.15)
ms:contentKeyID: 48545864
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052925
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 44329a4cc320e9adcc0612629bcc3fdcd179a1c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314879"
---
# <a name="tabledefvalidationrule-property-dao"></a><span data-ttu-id="b5b98-102">Propriedade TableDef.ValidationRule (DAO)</span><span class="sxs-lookup"><span data-stu-id="b5b98-102">TableDef.ValidationRule property (DAO)</span></span>

<span data-ttu-id="b5b98-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b5b98-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b5b98-104">Define ou retorna um valor que valida os dados em um campo à medida que estes são alterados ou adicionados a uma tabela (somente espaços de trabalho do Microsoft Access). **String** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="b5b98-104">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only).Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5b98-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5b98-105">Syntax</span></span>

<span data-ttu-id="b5b98-106">*expressão* . ValidationRule</span><span class="sxs-lookup"><span data-stu-id="b5b98-106">*expression* .ValidationRule</span></span>

<span data-ttu-id="b5b98-107">*expressão* Uma variável que representa um objeto **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="b5b98-107">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5b98-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="b5b98-108">Remarks</span></span>

<span data-ttu-id="b5b98-p101">As configurações ou valores de retorno são um **String** que descreve uma comparação no formulário de uma cláusula SQL WHERE sem a palavra reservada WHERE. Para um objeto ainda não acrescentado à coleção **Fields**, essa propriedade será leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="b5b98-p101">The settings or return values is a **String** that describes a comparison in the form of an SQL WHERE clause without the WHERE reserved word. For an object not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="b5b98-p102">A propriedade **ValidationRule** determina se um campo contém ou não dados válidos. Se os dados não forem válidos, ocorrerá um erro interceptável de tempo de execução. A mensagem de erro retornada será o texto da propriedade **ValidationText**, se especificado, ou o texto da expressão especificada por **ValidationRule**.</span><span class="sxs-lookup"><span data-stu-id="b5b98-p102">The **ValidationRule** property determines whether or not a field contains valid data. If the data is not valid, a trappable run-time error occurs. The returned error message is the text of the **ValidationText** property, if specified, or the text of the expression specified by **ValidationRule**.</span></span>

<span data-ttu-id="b5b98-114">Somente há suporte para a validação em bancos de dados que usam o mecanismo do banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="b5b98-114">Validation is supported only for databases that use the Microsoft Access database engine.</span></span>

<span data-ttu-id="b5b98-p103">A expressão da cadeia de caracteres especificada pela propriedade **ValidationRule** de um objeto **Field** pode se referir apenas a esse **Field** e não às funções definidas pelo usuário, às funções agregadas SQL ou às consultas. Para definir uma propriedade **ValidationRule** do objeto **Field** quando a definição da propriedade **ValidateOnSet** for **True**, a expressão deverá analisar com sucesso o nome do campo (com o nome do campo como um operando implícito) e avaliá-lo como **True**. Caso a definição da propriedade **ValidateOnSet** seja **False**, a definição da propriedade **ValidationRule** será ignorada.</span><span class="sxs-lookup"><span data-stu-id="b5b98-p103">The string expression specified by the **ValidationRule** property of a **Field** object can refer only to that **Field**. The expression can't refer to user-defined functions, SQL aggregate functions, or queries. To set a **Field** object's **ValidationRule** property when its **ValidateOnSet** property setting is **True**, the expression must successfully parse (with the field name as an implied operand) and evaluate to **True**. If its **ValidateOnSet** property setting is **False**, the **ValidationRule** property setting is ignored.</span></span>

<span data-ttu-id="b5b98-p104">A propriedade **ValidationRule** de um objeto **Recordset** ou **TableDef** pode se referir a vários campos desse objeto. As restrições observadas anteriormente neste tópico do objeto **Field** são aplicáveis.</span><span class="sxs-lookup"><span data-stu-id="b5b98-p104">The **ValidationRule** property of a **Recordset** or **TableDef** object can refer to multiple fields in that object. The restrictions noted earlier in this topic for the **Field** object apply.</span></span>

<span data-ttu-id="b5b98-p105">Para um objeto **TableDef** baseado em uma tabela vinculada, a propriedade **ValidationRule** herda a definição da propriedade **ValidationRule** da tabela base. Se a tabela base não oferecer suporte à validação, o valor dessa propriedade será uma sequência com comprimento zero ("").</span><span class="sxs-lookup"><span data-stu-id="b5b98-p105">For a **TableDef** object based on an linked table, the **ValidationRule** property inherits the **ValidationRule** property setting of the underlying base table. If the underlying base table doesn't support validation, the value of this property is a zero-length string ("").</span></span>

> [!NOTE]
> <span data-ttu-id="b5b98-123">Se você definir a propriedade como uma cadeia de caracteres concatenada com um valor não inteiro, e os parâmetros do sistema especificarem um valor não-americano. caractere decimal, como uma vírgula (por exemplo, strRule = "PRICE &gt; " &amp; lngPrice e lngPrice = 125,50), ocorrerá um erro quando seu código tentar validar quaisquer dados.</span><span class="sxs-lookup"><span data-stu-id="b5b98-123">If you set the property to a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strRule = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error will result when your code attempts to validate any data.</span></span> <span data-ttu-id="b5b98-124">Isso acontecerá porque durante a concatenação, o número será convertido em uma sequência que usa o caractere decimal padrão do sistema e o Microsoft Access SQL aceita somente os caracteres decimais do padrão dos EUA.</span><span class="sxs-lookup"><span data-stu-id="b5b98-124">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>
