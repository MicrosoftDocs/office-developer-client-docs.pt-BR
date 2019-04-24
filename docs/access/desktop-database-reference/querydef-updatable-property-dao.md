---
title: Propriedade QueryDef. upDatable (DAO)
TOCTitle: Updatable Property
ms:assetid: 9b978b7d-1d76-ff27-a032-dd94660fb088
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198056(v=office.15)
ms:contentKeyID: 48546575
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c5321e834f1dd5ed663033cacb530962d7beeb5a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303329"
---
# <a name="querydefupdatable-property-dao"></a><span data-ttu-id="37006-102">Propriedade QueryDef. upDatable (DAO)</span><span class="sxs-lookup"><span data-stu-id="37006-102">QueryDef.Updatable property (DAO)</span></span>


<span data-ttu-id="37006-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="37006-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="37006-104">Retorna um valor que indica se você pode alterar um objeto DAO.</span><span class="sxs-lookup"><span data-stu-id="37006-104">Returns a value that indicates whether you can change a DAO object.</span></span> <span data-ttu-id="37006-105">**Boolean** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="37006-105">Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="37006-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="37006-106">Syntax</span></span>

<span data-ttu-id="37006-107">*expressão* . Atualizável</span><span class="sxs-lookup"><span data-stu-id="37006-107">*expression* .Updatable</span></span>

<span data-ttu-id="37006-108">*expressão* Uma variável que representa um objeto **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="37006-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="37006-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="37006-109">Remarks</span></span>

<span data-ttu-id="37006-110">A propriedade **Updatable** de um objeto **QueryDef** será definida como **True** se a definição da consulta puder ser atualizada, mesmo que o objeto **[Recordset](recordset-object-dao.md)** resultante não seja atualizável.</span><span class="sxs-lookup"><span data-stu-id="37006-110">The **Updatable** property of a **QueryDef** object is set to **True** if the query definition can be updated, even if the resulting **[Recordset](recordset-object-dao.md)** object isn't updatable.</span></span>

