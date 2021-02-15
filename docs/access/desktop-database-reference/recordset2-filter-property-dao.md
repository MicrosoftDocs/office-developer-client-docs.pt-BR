---
title: Propriedade Recordset2.Filter (DAO)
TOCTitle: Filter Property
ms:assetid: 5b3b4e18-8af4-5acd-a129-513ba2d913d1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194529(v=office.15)
ms:contentKeyID: 48545069
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053062
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 19f3c017aa5d4a353f3e832a3678d921565ea822
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307326"
---
# <a name="recordset2filter-property-dao"></a><span data-ttu-id="c2d01-102">Propriedade Recordset2.Filter (DAO)</span><span class="sxs-lookup"><span data-stu-id="c2d01-102">Recordset2.Filter property (DAO)</span></span>


<span data-ttu-id="c2d01-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c2d01-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c2d01-104">Define ou retorna um valor que determina os registros incluídos em um objeto **Recordset** aberto posteriormente (somente nos espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="c2d01-104">Sets or returns a value that determines the records included in a subsequently opened **Recordset** object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="c2d01-105">**String** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c2d01-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2d01-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c2d01-106">Syntax</span></span>

<span data-ttu-id="c2d01-107">*expressão* . Filter</span><span class="sxs-lookup"><span data-stu-id="c2d01-107">*expression* .Filter</span></span>

<span data-ttu-id="c2d01-108">*expressão* Uma expressão que retorna um **objeto Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="c2d01-108">*expression* An expression that returns a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2d01-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2d01-109">Remarks</span></span>

<span data-ttu-id="c2d01-110">O valor de definição ou de retorno é um tipo de dados de cadeia de caracteres que contém a cláusula WHERE de uma instrução SQL sem a palavra reservada WHERE.</span><span class="sxs-lookup"><span data-stu-id="c2d01-110">The setting or return value is a String data type that contains the WHERE clause of an SQL statement without the reserved word WHERE.</span></span>

<span data-ttu-id="c2d01-111">Use a propriedade **Filter** para aplicar um filtro a um objeto **Recordset** do tipo dynaset, instantâneo ou somente encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="c2d01-111">Use the **Filter** property to apply a filter to a dynaset–, snapshot–, or forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="c2d01-112">Você pode usar a propriedade **Filter** para restringir os registros retornados de um objeto existente quando um novo objeto **Recordset** for aberto com base em um objeto **Recordset** existente.</span><span class="sxs-lookup"><span data-stu-id="c2d01-112">You can use the **Filter** property to restrict the records returned from an existing object when a new **Recordset** object is opened based on an existing **Recordset** object.</span></span>

<span data-ttu-id="c2d01-113">Use o formato de dados dos EUA (mês-dia-ano) quando você filtra campos com datas, mesmo se você não estiver usando a versão dos EUA do mecanismo de banco de dados do Microsoft Access (nesse caso, você deverá montar todas as datas ao concatenar cadeias de caracteres, por exemplo, strMonth & "-" & strDay & "-" & strYear).</span><span class="sxs-lookup"><span data-stu-id="c2d01-113">Use the U.S. date format (month-day-year) when you filter fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine (in which case you must assemble any dates by concatenating strings, for example, strMonth & "-" & strDay & "-" & strYear).</span></span> <span data-ttu-id="c2d01-114">Caso contrário, é possível que os dados não sejam filtrados como esperado.</span><span class="sxs-lookup"><span data-stu-id="c2d01-114">Otherwise, the data may not be filtered as you expect.</span></span>

<span data-ttu-id="c2d01-115">Em vários casos, é mais rápido abrir um novo objeto **Recordset** usando uma instrução SQL que inclua uma cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="c2d01-115">In many cases, it's faster to open a new **Recordset** object by using an SQL statement that includes a WHERE clause.</span></span>

<span data-ttu-id="c2d01-116">Se você definir a propriedade como uma cadeia de caracteres concatenada com um valor não inteiro, e se os parâmetros do sistema especificarem um caractere decimal não americano, como uma vírgula (por exemplo, strFilter = "PRICE > \>" & lngPrice e lngPrice = 125,50), ocorrerá um erro quando você tentar abrir o próximo **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="c2d01-116">If you set the property to a string concatenated with a non–integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strFilter = "PRICE \> " & lngPrice, and lngPrice = 125,50), an error occurs when you try to open the next **Recordset**.</span></span> <span data-ttu-id="c2d01-117">Isso acontecerá porque durante a concatenação, o número será convertido em uma sequência que usa o caractere decimal padrão do sistema e o Microsoft Access SQL aceita somente os caracteres decimais do padrão dos EUA.</span><span class="sxs-lookup"><span data-stu-id="c2d01-117">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

