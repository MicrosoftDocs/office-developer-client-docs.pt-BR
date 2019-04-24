---
title: Propriedade Recordset2. Filter (DAO)
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
# <a name="recordset2filter-property-dao"></a><span data-ttu-id="4043d-102">Propriedade Recordset2. Filter (DAO)</span><span class="sxs-lookup"><span data-stu-id="4043d-102">Recordset2.Filter property (DAO)</span></span>


<span data-ttu-id="4043d-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4043d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4043d-104">Define ou retorna um valor que determina os registros incluídos em um objeto **Recordset** aberto posteriormente (somente nos espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="4043d-104">Sets or returns a value that determines the records included in a subsequently opened **Recordset** object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="4043d-105">**String** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="4043d-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4043d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4043d-106">Syntax</span></span>

<span data-ttu-id="4043d-107">*expressão* . Filtre</span><span class="sxs-lookup"><span data-stu-id="4043d-107">*expression* .Filter</span></span>

<span data-ttu-id="4043d-108">*expressão* Uma expressão que retorna um objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="4043d-108">*expression* An expression that returns a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4043d-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="4043d-109">Remarks</span></span>

<span data-ttu-id="4043d-110">O valor de definição ou de retorno é um tipo de dados de cadeia de caracteres que contém a cláusula WHERE de uma instrução SQL sem a palavra reservada WHERE.</span><span class="sxs-lookup"><span data-stu-id="4043d-110">The setting or return value is a String data type that contains the WHERE clause of an SQL statement without the reserved word WHERE.</span></span>

<span data-ttu-id="4043d-111">Use a propriedade **Filter** para aplicar um filtro a um objeto **Recordset** do tipo dynaset, instantâneo ou somente encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="4043d-111">Use the **Filter** property to apply a filter to a dynaset–, snapshot–, or forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="4043d-112">Você pode usar a propriedade **Filter** para restringir os registros retornados de um objeto existente quando um novo objeto **Recordset** for aberto com base em um objeto **Recordset** existente.</span><span class="sxs-lookup"><span data-stu-id="4043d-112">You can use the **Filter** property to restrict the records returned from an existing object when a new **Recordset** object is opened based on an existing **Recordset** object.</span></span>

<span data-ttu-id="4043d-113">Use o formato de data dos EUA (mês-dia-ano) quando você filtrar campos que contenham datas, mesmo que não esteja usando a versão norte-americana do mecanismo de banco de dados do Microsoft Access (nesse caso, você deve montar qualquer data por meio da concatenação de cadeias de caracteres, por exemplo, strMonth & "-" _ aMP_ strDay & "-" & strYear).</span><span class="sxs-lookup"><span data-stu-id="4043d-113">Use the U.S. date format (month-day-year) when you filter fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine (in which case you must assemble any dates by concatenating strings, for example, strMonth & "-" & strDay & "-" & strYear).</span></span> <span data-ttu-id="4043d-114">Caso contrário, é possível que os dados não sejam filtrados como esperado.</span><span class="sxs-lookup"><span data-stu-id="4043d-114">Otherwise, the data may not be filtered as you expect.</span></span>

<span data-ttu-id="4043d-115">Em muitos casos, é mais rápido abrir um novo objeto **Recordset** pelo uso de uma instrução SQL que inclui a cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="4043d-115">In many cases, it's faster to open a new **Recordset** object by using an SQL statement that includes a WHERE clause.</span></span>

<span data-ttu-id="4043d-116">Se você definir a propriedade como uma cadeia de caracteres concatenada com um valor não inteiro e os parâmetros do sistema especificarem um caractere não norte-americano. decimal, como vírgula (por exemplo, strFilter = "PRICE \> " & lngPrice e lngPrice = 125, 50), ocorrerá um erro quando você tentar Abra o próximo **conjunto de registros**.</span><span class="sxs-lookup"><span data-stu-id="4043d-116">If you set the property to a string concatenated with a non–integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strFilter = "PRICE \> " & lngPrice, and lngPrice = 125,50), an error occurs when you try to open the next **Recordset**.</span></span> <span data-ttu-id="4043d-117">Isso acontecerá porque durante a concatenação, o número será convertido em uma sequência que usa o caractere decimal padrão do sistema e o Microsoft Access SQL aceita somente os caracteres decimais do padrão dos EUA.</span><span class="sxs-lookup"><span data-stu-id="4043d-117">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

