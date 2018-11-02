---
title: Propriedade Index.Clustered (DAO)
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
ms.openlocfilehash: 4e7bd39d3329c83ec2a26fbef11e3a3b4e51e760
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921297"
---
# <a name="indexclustered-property-dao"></a><span data-ttu-id="d7414-102">Propriedade Index.Clustered (DAO)</span><span class="sxs-lookup"><span data-stu-id="d7414-102">Index.Clustered property (DAO)</span></span>


<span data-ttu-id="d7414-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="d7414-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d7414-p101">Define ou retorna um valor que indica se um objeto **Index** representa um índice agrupado para uma tabela (apenas espaços de trabalho do Microsoft Access). **Boolean** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="d7414-p101">Sets or returns a value that indicates whether an **Index** object represents a clustered index for a table (Microsoft Access workspaces only). Read/write **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7414-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d7414-106">Syntax</span></span>

<span data-ttu-id="d7414-107">*expressão* . Em cluster</span><span class="sxs-lookup"><span data-stu-id="d7414-107">*expression* .Clustered</span></span>

<span data-ttu-id="d7414-108">*expressão* Uma expressão que retorna um objeto **Index** .</span><span class="sxs-lookup"><span data-stu-id="d7414-108">*expression* An expression that returns a **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7414-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7414-109">Remarks</span></span>

<span data-ttu-id="d7414-110">O valor definido ou retornado é um tipo de dados Booliano que será **True** se o objeto **Index** representar um índice agrupado.</span><span class="sxs-lookup"><span data-stu-id="d7414-110">The setting or return value is a Boolean data type that is **True** if the **Index** object represents a clustered index.</span></span>

<span data-ttu-id="d7414-p102">Alguns formatos de banco de dados de desktop IISAM usam índices agrupados que consistem em um ou mais campos não-chave que juntos organizam todos os registros de uma tabela em uma ordem predefinida. Um índice agrupado fornece acesso eficiente aos registros em uma tabela nos quais os valores de índice podem não ser exclusivos.</span><span class="sxs-lookup"><span data-stu-id="d7414-p102">Some IISAM desktop database formats use clustered indexes. A clustered index consists of one or more nonkey fields that, taken together, arrange all records in a table in a predefined order. A clustered index provides efficient access to records in a table in which the index values may not be unique.</span></span>

<span data-ttu-id="d7414-114">A propriedade **Clustered** é de leitura/gravação para um novo objeto **Index** ainda não acrescentado a uma coleção e somente leitura para um objeto **Index** existente em uma coleção **Indexes**.</span><span class="sxs-lookup"><span data-stu-id="d7414-114">The **Clustered** property is read/write for a new **Index** object not yet appended to a collection and read-only for an existing **Index** object in an **Indexes** collection.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="d7414-115">Os bancos de dados do mecanismo de banco de dados do Microsoft Access ignoram a propriedade <STRONG>Clustered</STRONG> porque esse mecanismo não fornece suporte a índices agrupados.</span><span class="sxs-lookup"><span data-stu-id="d7414-115">Microsoft Access database engine databases ignore the <STRONG>Clustered</STRONG> property because the Microsoft Access database engine doesn't support clustered indexes.</span></span></P>
> <LI>
> <P><span data-ttu-id="d7414-116">Para fontes de dados ODBC, a propriedade <STRONG>Clustered</STRONG> sempre retorna <STRONG>False</STRONG>; ele não detecta se a fonte de dados ODBC tem um índice agrupado ou não.</span><span class="sxs-lookup"><span data-stu-id="d7414-116">For ODBC data sources the <STRONG>Clustered</STRONG> property always returns <STRONG>False</STRONG>; it does not detect whether or not the ODBC data source has a clustered index.</span></span></P></LI></UL>


