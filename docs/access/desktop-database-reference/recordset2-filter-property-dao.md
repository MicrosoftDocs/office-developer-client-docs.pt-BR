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
ms.openlocfilehash: 9be017367a0422884e393acf82d96e6b4908689a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876446"
---
# <a name="recordset2filter-property-dao"></a><span data-ttu-id="0bd90-102">Propriedade Recordset2.Filter (DAO)</span><span class="sxs-lookup"><span data-stu-id="0bd90-102">Recordset2.Filter Property (DAO)</span></span>


<span data-ttu-id="0bd90-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="0bd90-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0bd90-p101">Define ou retornar um valor que determina os registros incluídos em um objeto **Recordset** aberto subsequentemente (somente espaços de trabalho do Microsoft Access). **String** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="0bd90-p101">Sets or returns a value that determines the records included in a subsequently opened **Recordset** object (Microsoft Access workspaces only). Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bd90-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0bd90-106">Syntax</span></span>

<span data-ttu-id="0bd90-107">*expressão* . Filtro</span><span class="sxs-lookup"><span data-stu-id="0bd90-107">*expression* .Filter</span></span>

<span data-ttu-id="0bd90-108">*expressão* Uma expressão que retorna um objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="0bd90-108">*expression* An expression that returns a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bd90-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="0bd90-109">Remarks</span></span>

<span data-ttu-id="0bd90-110">O valor de definição ou de retorno é um tipo de dados de cadeia de caracteres que contém a cláusula WHERE de uma instrução SQL sem a palavra reservada WHERE.</span><span class="sxs-lookup"><span data-stu-id="0bd90-110">The setting or return value is a String data type that contains the WHERE clause of an SQL statement without the reserved word WHERE.</span></span>

<span data-ttu-id="0bd90-111">Use a propriedade **Filter** para aplicar um filtro a um dynaset, instantâneo ou objeto **Recordset** do tipo somente encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="0bd90-111">Use the **Filter** property to apply a filter to a dynaset–, snapshot–, or forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="0bd90-112">Você pode usar a propriedade **Filter** para restringir os registros retornados de um objeto existente quando um novo objeto **Recordset** for aberto com base em um objeto **Recordset** existente.</span><span class="sxs-lookup"><span data-stu-id="0bd90-112">You can use the **Filter** property to restrict the records returned from an existing object when a new **Recordset** object is opened based on an existing **Recordset** object.</span></span>

<span data-ttu-id="0bd90-113">Utilize o formato de data dos EUA (mês-dia-ano) quando filtrar campos que contenham datas, mesmo se você não estiver usando a versão EUA do mecanismo de banco de dados do Microsoft Access (nesse caso, você deve montar quaisquer datas concatenando cadeias de caracteres, por exemplo, strMonth & "-" & strDay & "-" & strYear).</span><span class="sxs-lookup"><span data-stu-id="0bd90-113">Use the U.S. date format (month-day-year) when you filter fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine (in which case you must assemble any dates by concatenating strings, for example, strMonth & "-" & strDay & "-" & strYear).</span></span> <span data-ttu-id="0bd90-114">Caso contrário, é possível que os dados não sejam filtrados como esperado.</span><span class="sxs-lookup"><span data-stu-id="0bd90-114">Otherwise, the data may not be filtered as you expect.</span></span>

<span data-ttu-id="0bd90-115">Em vários casos, é mais rápido abrir um novo objeto **Recordset** usando uma instrução SQL que inclua uma cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="0bd90-115">In many cases, it's faster to open a new **Recordset** object by using an SQL statement that includes a WHERE clause.</span></span>

<span data-ttu-id="0bd90-116">Se você definir a propriedade como uma cadeia de caracteres concatenada com um valor não – inteiro e os parâmetros do sistema especificarem um caractere decimal que fora dos EUA, como uma vírgula (por exemplo, strFilter = "preço \> " & lngPrice e lngPrice = 125,50), ocorrerá um erro ao tentar Abra o próximo **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="0bd90-116">If you set the property to a string concatenated with a non–integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strFilter = "PRICE \> " & lngPrice, and lngPrice = 125,50), an error occurs when you try to open the next **Recordset**.</span></span> <span data-ttu-id="0bd90-117">Isso acontecerá porque durante a concatenação, o número será convertido em uma sequência que usa o caractere decimal padrão do sistema e o Microsoft Access SQL aceita somente os caracteres decimais do padrão dos EUA.</span><span class="sxs-lookup"><span data-stu-id="0bd90-117">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

