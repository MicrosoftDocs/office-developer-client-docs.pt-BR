---
title: Seção SQL do arquivo de personalização
TOCTitle: Customization File SQL section
ms:assetid: 002c544f-fe1b-6aeb-ba9a-97b1e1159516
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248776(v=office.15)
ms:contentKeyID: 48542901
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8ae259589cc8d4945068901c59105425599edc64
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295132"
---
# <a name="customization-file-sql-section"></a><span data-ttu-id="849cb-102">Seção SQL do arquivo de personalização</span><span class="sxs-lookup"><span data-stu-id="849cb-102">Customization File SQL section</span></span>


<span data-ttu-id="849cb-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="849cb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="849cb-p101">A seção **sql** pode conter uma nova sequência de caracteres SQL que substitui a sequência de comando do cliente. Se a seção não tiver nenhuma sequência de caracteres SQL, ela será ignorada.</span><span class="sxs-lookup"><span data-stu-id="849cb-p101">The **sql** section can contain a new SQL string that replaces the client command string. If there is no SQL string in the section, the section will be ignored.</span></span>

<span data-ttu-id="849cb-p102">A nova sequência de caracteres SQL pode conter parâmetros. Isso significa que os parâmetros na sequência de caracteres SQL da seção **sql** (designada pelo caractere '?') podem ser substituídos pelos argumentos correspondentes em um *identifier* na sequência de comando do cliente (designada por uma lista delimitada por vírgula entre parênteses). O identificador e a lista de argumentos funcionam como uma chamada de função.</span><span class="sxs-lookup"><span data-stu-id="849cb-p102">The new SQL string may be *parameterized*. That is, parameters in the **sql** section SQL string (designated by the '?' character) can be replaced by corresponding arguments in an *identifier* in the client command string (designated by a comma-delimited list in parentheses). The identifier and argument list behave like a function call.</span></span>

<span data-ttu-id="849cb-109">Por exemplo, suponha que a cadeia de comando do cliente seja "CustomerByID(4)" , o header da seção SQL seja SQL CustomerByID e a nova cadeia de caracteres da seção SQL seja \[ \] "SELECT \* FROM Customers WHERE CustomerID = ?".</span><span class="sxs-lookup"><span data-stu-id="849cb-109">For example, assume the client command string is "CustomerByID(4)" , the SQL section header is \[SQL CustomerByID\] , and the new SQL section string is "SELECT \* FROM Customers WHERE CustomerID = ?".</span></span> <span data-ttu-id="849cb-110">O manipulador gerará , o header da seção SQL é SQL CustomerByID e a nova cadeia de caracteres de seção SQL é \[ \] "SELECT \* FROM Customers WHERE CustomerID = ?".</span><span class="sxs-lookup"><span data-stu-id="849cb-110">The Handler will generate , the SQL section header is \[SQL CustomerByID\] , and the new SQL section string is "SELECT \* FROM Customers WHERE CustomerID = ?".</span></span> <span data-ttu-id="849cb-111">O manipulador gerará "SELECT FROM Customers WHERE CustomerID = 4" e usará essa cadeia de caracteres \* para consultar a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="849cb-111">The Handler will generate "SELECT \* FROM Customers WHERE CustomerID = 4" and use that string to query the data source.</span></span>

<span data-ttu-id="849cb-112">Se a nova sequência de caracteres SQL for a sequência nula (""), a seção será ignorada.</span><span class="sxs-lookup"><span data-stu-id="849cb-112">If the new SQL statement is the null string (""), then the section is ignored.</span></span>

<span data-ttu-id="849cb-p104">Se a nova sequência de caracteres SQL for inválida, a execução da instrução não ocorrerá e o parâmetro cliente será efetivamente ignorado. Você pode executar esse procedimento de forma intencional para "desativar" todos os comandos SQL de cliente especificando:</span><span class="sxs-lookup"><span data-stu-id="849cb-p104">If the new SQL statement string is not valid, then the execution of the statement will fail. The client parameter is effectively ignored. You can do this intentionally to "turn off" all client SQL commands by specifying:</span></span>

```sql 
 
[SQL default] 
SQL = " " 
```

## <a name="syntax"></a><span data-ttu-id="849cb-116">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="849cb-116">Syntax</span></span>

<span data-ttu-id="849cb-117">Uma entrada de sequência de caracteres SQL de substituição tem este formato:</span><span class="sxs-lookup"><span data-stu-id="849cb-117">A replacement SQL string entry is of the form:</span></span>

<span data-ttu-id="849cb-118">**SQL=\*sqlString**\*</span><span class="sxs-lookup"><span data-stu-id="849cb-118">**SQL=\*sqlString**\*</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="849cb-119">Sair</span><span class="sxs-lookup"><span data-stu-id="849cb-119">Part</span></span></p></th>
<th><p><span data-ttu-id="849cb-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="849cb-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="849cb-121"><strong>SQL</strong></span><span class="sxs-lookup"><span data-stu-id="849cb-121"><strong>SQL</strong></span></span></p></td>
<td><p><span data-ttu-id="849cb-122">Uma sequência literal que indica uma entrada de seção SQL.</span><span class="sxs-lookup"><span data-stu-id="849cb-122">A literal string that indicates this is an SQL section entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="849cb-123"><strong><em>sqlString</em></strong></span><span class="sxs-lookup"><span data-stu-id="849cb-123"><strong><em>sqlString</em></strong></span></span></p></td>
<td><p><span data-ttu-id="849cb-124">Uma sequência de caracteres SQL que substitui a sequência de caracteres do cliente.</span><span class="sxs-lookup"><span data-stu-id="849cb-124">An SQL string that replaces the client string.</span></span></p></td>
</tr>
</tbody>
</table>

