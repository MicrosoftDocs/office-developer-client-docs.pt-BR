---
title: Localizar o método - ActiveX Data Objects (ADO)
TOCTitle: Find Method (ADO)
ms:assetid: a7cc9ceb-fdb9-73e2-8328-70b174f93cda
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249776(v=office.15)
ms:contentKeyID: 48546887
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fc78503008daa733e747923697f21917ada8c106
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463270"
---
# <a name="find-method-ado"></a><span data-ttu-id="07925-102">Método Find (ADO)</span><span class="sxs-lookup"><span data-stu-id="07925-102">Find Method (ADO)</span></span>


<span data-ttu-id="07925-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="07925-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="07925-p101">Procura um [Recordset](recordset-object-ado.md) para a linha que satisfaz os critérios especificados. Opcionalmente, a direção da pesquisa, a linha inicial e o deslocamento a partir da linha inicial podem ser especificados. Se os critérios forem atendidos, a posição da linha atual é definida no registro encontrado; caso contrário, a posição é definida para o final (ou início) do **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="07925-p101">Searches a [Recordset](recordset-object-ado.md) for the row that satisfies the specified criteria. Optionally, the direction of the search, starting row, and offset from the starting row may be specified. If the criteria is met, the current row position is set on the found record; otherwise, the position is set to the end (or start) of the **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="07925-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="07925-107">Syntax</span></span>

<span data-ttu-id="07925-108">Encontre (*critérios*, *SkipRows*, *SearchDirection*, *Iniciar*)</span><span class="sxs-lookup"><span data-stu-id="07925-108">Find (*Criteria*, *SkipRows*, *SearchDirection*, *Start*)</span></span>

## <a name="parameters"></a><span data-ttu-id="07925-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="07925-109">Parameters</span></span>

  - <span data-ttu-id="07925-110">*Criteria*</span><span class="sxs-lookup"><span data-stu-id="07925-110">*Criteria*</span></span>

  - <span data-ttu-id="07925-111">Um valor **String** que contém uma instrução que especifica o nome da coluna, o operador da comparação e o valor a ser utilizado na pesquisa.</span><span class="sxs-lookup"><span data-stu-id="07925-111">A **String** value that contains a statement specifying the column name, comparison operator, and value to use in the search.</span></span>

  - <span data-ttu-id="07925-112">*SkipRows*</span><span class="sxs-lookup"><span data-stu-id="07925-112">*SkipRows*</span></span>

  - <span data-ttu-id="07925-p102">Opcional *.* Um valor **Long**, cujo valor padrão é zero, que especifica o deslocamento de linha a partir da linha atual ou do indicador *Start* para iniciar a pesquisa. Por padrão, a pesquisa iniciará na linha atual.</span><span class="sxs-lookup"><span data-stu-id="07925-p102">Optional *.* A **Long** value, whose default value is zero, that specifies the row offset from the current row or *Start* bookmark to begin the search. By default, the search will start on the current row.</span></span>

  - <span data-ttu-id="07925-116">*SearchDirection*</span><span class="sxs-lookup"><span data-stu-id="07925-116">*SearchDirection*</span></span>

  - <span data-ttu-id="07925-p103">Opcional *.* Um valor [SearchDirectionEnum](searchdirectionenum.md) que especifica que a pesquisa deve iniciar na linha atual ou na próxima linha disponível na direção da pesquisa. Uma pesquisa sem êxito para no final do **Recordset** se o valor for **adSearchForward**. Uma pesquisa sem êxito para no início do **Recordset** se o valor for **adSearchBackward**.</span><span class="sxs-lookup"><span data-stu-id="07925-p103">Optional *.* A [SearchDirectionEnum](searchdirectionenum.md) value that specifies whether the search should begin on the current row or the next available row in the direction of the search. An unsuccessful search stops at the end of the **Recordset** if the value is **adSearchForward**. An unsuccessful search stops at the start of the **Recordset** if the value is **adSearchBackward**.</span></span>

  - <span data-ttu-id="07925-121">*Start*</span><span class="sxs-lookup"><span data-stu-id="07925-121">*Start*</span></span>

  - <span data-ttu-id="07925-p104">Opcional. Um indicador **Variant** que funciona como a posição inicial da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="07925-p104">Optional. A **Variant** bookmark that functions as the starting position for the search.</span></span>

## <a name="remarks"></a><span data-ttu-id="07925-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="07925-124">Remarks</span></span>

<span data-ttu-id="07925-p105">Apenas um único nome de coluna pode ser especificado em *criteria*. Este método não suporta pesquisas de várias colunas.</span><span class="sxs-lookup"><span data-stu-id="07925-p105">Only a single-column name may be specified in *criteria*. This method does not support multi-column searches.</span></span>

<span data-ttu-id="07925-127">O operador de comparação nos *critérios* pode ser "**\>**"(maior que),"**\<**"(menor que), "=" (igual a),"\>=" (maior que ou igual), "\<=" (menor ou igual), "\<\>" (não igual a), ou "como" (padrão correspondente).</span><span class="sxs-lookup"><span data-stu-id="07925-127">The comparison operator in *Criteria* may be "**\>**" (greater than), "**\<**" (less than), "=" (equal), "\>=" (greater than or equal), "\<=" (less than or equal), "\<\>" (not equal), or "like" (pattern matching).</span></span>

<span data-ttu-id="07925-128">O valor nos *critérios* pode ser uma cadeia de caracteres, número de ponto flutuante ou data.</span><span class="sxs-lookup"><span data-stu-id="07925-128">The value in *Criteria* may be a string, floating-point number, or date.</span></span> <span data-ttu-id="07925-129">Valores de cadeia de caracteres são delimitados por aspas simples ou "\#" (sinal numérico) marca (por exemplo, "estado = 'WA'" ou "estado = \#WA\#").</span><span class="sxs-lookup"><span data-stu-id="07925-129">String values are delimited with single quotes or "\#" (number sign) marks (for example, "state = 'WA'" or "state = \#WA\#").</span></span> <span data-ttu-id="07925-130">Valores de data são delimitados por "\#" (sinal numérico) marca (por exemplo, "Iniciar\_data \> \#22/7/97\#") e pode conter horas, minutos e segundos para indicar carimbos de tempo, mas não devem conter milissegundos ou ocorrerão erros .</span><span class="sxs-lookup"><span data-stu-id="07925-130">Date values are delimited with "\#" (number sign) marks (for example, "start\_date \> \#7/22/97\#") and can contain hours, minutes and seconds to indicate time stamps but should not contain milliseconds or errors will occur.</span></span>

<span data-ttu-id="07925-p107">Se o operador de comparação for "like", o valor da sequência poderá conter um asterisco (\*) para localizar uma ou mais ocorrências de qualquer caractere ou subsequência. Por exemplo, "state like 'M\*'" corresponde a Maine e Massachusetts. Também é possível utilizar asteriscos à esquerda e à direita para localizar uma subsequência contida nos valores. Por exemplo, "state like '\*as\*'" corresponde a Alaska, Arkansas e Massachusetts.</span><span class="sxs-lookup"><span data-stu-id="07925-p107">If the comparison operator is "like", the string value may contain an asterisk (\*) to find one or more occurrences of any character or substring. For example, "state like 'M\*'" matches Maine and Massachusetts. You can also use leading and trailing asterisks to find a substring contained within the values. For example, "state like '\*as\*'" matches Alaska, Arkansas, and Massachusetts.</span></span>

<span data-ttu-id="07925-p108">Os asteriscos podem ser utilizados apenas no final de uma sequência de critérios ou em conjunto, tanto no início quanto no final de uma sequência de critérios, conforme mostrado acima. Não é possível utilizar o asterisco como um caractere curinga inicial ('\*str') ou como caractere curinga incorporado ('s\*r'). Isso causará um erro.</span><span class="sxs-lookup"><span data-stu-id="07925-p108">Asterisks can be used only at the end of a criteria string, or together at both the beginning and end of a criteria string, as shown above. You cannot use the asterisk as a leading wildcard ('\*str'), or embedded wildcard ('s\*r'). This will cause an error.</span></span>


> [!NOTE]
> <P><span data-ttu-id="07925-p109">[!OBSERVAçãO] Ocorrerá um erro se uma posição de linha atual não for definida antes de chamar <STRONG>Find</STRONG>. Qualquer método que defina posição de linha, tal como <A href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</A>, deve ser chamado antes de chamar <STRONG>Find</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="07925-p109">An error will occur if a current row position is not set before calling <STRONG>Find</STRONG>. Any method that sets row position, such as <A href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</A>, should be called before calling <STRONG>Find</STRONG>.</span></span></P>




> [!NOTE]
> <P><span data-ttu-id="07925-p110">[!OBSERVAçãO] Se você chamar o método <STRONG>Find</STRONG> em um recordset e a posição atual no recordset estiver no último registro ou no final do arquivo (EOF), nada será encontrado. É necessário chamar o método <STRONG>MoveFirst</STRONG> para definir a posição atual/cursor para o início do recordset.</span><span class="sxs-lookup"><span data-stu-id="07925-p110">If you call the <STRONG>Find</STRONG> method on a recordset, and the current position in the recordset is at the last record or end of file (EOF), you will not find anything. You need to call the <STRONG>MoveFirst</STRONG> method to set the current position/cursor to the beginning of the recordset.</span></span></P>


