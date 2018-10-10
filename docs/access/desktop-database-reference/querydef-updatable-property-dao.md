---
title: Propriedade QueryDef.Updatable (DAO)
TOCTitle: Updatable Property
ms:assetid: 9b978b7d-1d76-ff27-a032-dd94660fb088
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198056(v=office.15)
ms:contentKeyID: 48546575
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6ca30e86bd61bc5459a552423bd451c7b158996d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462236"
---
# <a name="querydefupdatable-property-dao"></a><span data-ttu-id="bbc7f-102">Propriedade QueryDef.Updatable (DAO)</span><span class="sxs-lookup"><span data-stu-id="bbc7f-102">QueryDef.Updatable Property (DAO)</span></span>


<span data-ttu-id="bbc7f-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="bbc7f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="bbc7f-p101">Retorna um valor que indica se você pode alterar um objeto DAO. **Boolean** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="bbc7f-p101">Returns a value that indicates whether you can change a DAO object. Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbc7f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bbc7f-106">Syntax</span></span>

<span data-ttu-id="bbc7f-107">*expressão* . Atualizável</span><span class="sxs-lookup"><span data-stu-id="bbc7f-107">*expression* .Updatable</span></span>

<span data-ttu-id="bbc7f-108">*expressão* Uma variável que representa um objeto **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="bbc7f-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbc7f-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="bbc7f-109">Remarks</span></span>

<span data-ttu-id="bbc7f-110">A propriedade **Updatable** de um objeto **QueryDef** será definida como **True** se a definição da consulta puder ser atualizada, mesmo que o objeto **[Recordset](recordset-object-dao.md)** resultante não seja atualizável.</span><span class="sxs-lookup"><span data-stu-id="bbc7f-110">The **Updatable** property of a **QueryDef** object is set to **True** if the query definition can be updated, even if the resulting **[Recordset](recordset-object-dao.md)** object isn't updatable.</span></span>

