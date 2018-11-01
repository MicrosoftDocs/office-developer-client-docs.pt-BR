---
title: Propriedade QueryDef.Updatable (DAO)
TOCTitle: Updatable Property
ms:assetid: 9b978b7d-1d76-ff27-a032-dd94660fb088
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198056(v=office.15)
ms:contentKeyID: 48546575
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4ad761c2941cb556ce67c9f716247663220f753f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873688"
---
# <a name="querydefupdatable-property-dao"></a><span data-ttu-id="395ad-102">Propriedade QueryDef.Updatable (DAO)</span><span class="sxs-lookup"><span data-stu-id="395ad-102">QueryDef.Updatable Property (DAO)</span></span>


<span data-ttu-id="395ad-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="395ad-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="395ad-p101">Retorna um valor que indica se você pode alterar um objeto DAO. **Boolean** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="395ad-p101">Returns a value that indicates whether you can change a DAO object. Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="395ad-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="395ad-106">Syntax</span></span>

<span data-ttu-id="395ad-107">*expressão* . Atualizável</span><span class="sxs-lookup"><span data-stu-id="395ad-107">*expression* .Updatable</span></span>

<span data-ttu-id="395ad-108">*expressão* Uma variável que representa um objeto **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="395ad-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="395ad-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="395ad-109">Remarks</span></span>

<span data-ttu-id="395ad-110">A propriedade **Updatable** de um objeto **QueryDef** será definida como **True** se a definição da consulta puder ser atualizada, mesmo que o objeto **[Recordset](recordset-object-dao.md)** resultante não seja atualizável.</span><span class="sxs-lookup"><span data-stu-id="395ad-110">The **Updatable** property of a **QueryDef** object is set to **True** if the query definition can be updated, even if the resulting **[Recordset](recordset-object-dao.md)** object isn't updatable.</span></span>

