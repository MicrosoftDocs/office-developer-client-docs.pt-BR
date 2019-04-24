---
title: Propriedade index. Clustered (DAO)
TOCTitle: Clustered Property
ms:assetid: dd0876a9-b7fe-c8c8-e675-5ed758ce5bd3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835375(v=office.15)
ms:contentKeyID: 48548149
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052930
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 060963dc47c933fee903cd9b220adb45c7f63df6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291849"
---
# <a name="indexclustered-property-dao"></a><span data-ttu-id="cf9b6-102">Propriedade index. Clustered (DAO)</span><span class="sxs-lookup"><span data-stu-id="cf9b6-102">Index.Clustered property (DAO)</span></span>

<span data-ttu-id="cf9b6-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cf9b6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cf9b6-p101">Define ou retorna um valor que indica se um objeto **Index** representa um índice agrupado para uma tabela (apenas espaços de trabalho do Microsoft Access). **Boolean** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="cf9b6-p101">Sets or returns a value that indicates whether an **Index** object represents a clustered index for a table (Microsoft Access workspaces only). Read/write **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf9b6-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cf9b6-106">Syntax</span></span>

<span data-ttu-id="cf9b6-107">*expressão* . Agrupado</span><span class="sxs-lookup"><span data-stu-id="cf9b6-107">*expression* .Clustered</span></span>

<span data-ttu-id="cf9b6-108">*expressão* Uma expressão que retorna um objeto **index** .</span><span class="sxs-lookup"><span data-stu-id="cf9b6-108">*expression* An expression that returns a **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf9b6-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf9b6-109">Remarks</span></span>

<span data-ttu-id="cf9b6-110">O valor definido ou retornado é um tipo de dados Booliano que será **True** se o objeto **Index** representar um índice agrupado.</span><span class="sxs-lookup"><span data-stu-id="cf9b6-110">The setting or return value is a Boolean data type that is **True** if the **Index** object represents a clustered index.</span></span>

<span data-ttu-id="cf9b6-p102">Alguns formatos de banco de dados de desktop IISAM usam índices agrupados que consistem em um ou mais campos não-chave que juntos organizam todos os registros de uma tabela em uma ordem predefinida. Um índice agrupado fornece acesso eficiente aos registros em uma tabela nos quais os valores de índice podem não ser exclusivos.</span><span class="sxs-lookup"><span data-stu-id="cf9b6-p102">Some IISAM desktop database formats use clustered indexes. A clustered index consists of one or more nonkey fields that, taken together, arrange all records in a table in a predefined order. A clustered index provides efficient access to records in a table in which the index values may not be unique.</span></span>

<span data-ttu-id="cf9b6-114">A propriedade **Clustered** é de leitura/gravação para um novo objeto **Index** ainda não acrescentado a uma coleção e somente leitura para um objeto **Index** existente em uma coleção **Indexes**.</span><span class="sxs-lookup"><span data-stu-id="cf9b6-114">The **Clustered** property is read/write for a new **Index** object not yet appended to a collection and read-only for an existing **Index** object in an **Indexes** collection.</span></span>

> [!NOTE]
> - <span data-ttu-id="cf9b6-115">Os bancos de dados do mecanismo de banco de dados do Microsoft Access ignoram a propriedade **Clustered** porque esse mecanismo não fornece suporte a índices agrupados.</span><span class="sxs-lookup"><span data-stu-id="cf9b6-115">Microsoft Access database engine databases ignore the **Clustered** property because the Microsoft Access database engine doesn't support clustered indexes.</span></span>
> - <span data-ttu-id="cf9b6-116">Para fontes de dados ODBC, \*\*\*\* a propriedade Clustered sempre retorna **false**; Ele não detecta se a fonte de dados ODBC tem um índice agrupado ou não.</span><span class="sxs-lookup"><span data-stu-id="cf9b6-116">For ODBC data sources, the **Clustered** property always returns **False**; it does not detect whether or not the ODBC data source has a clustered index.</span></span>


