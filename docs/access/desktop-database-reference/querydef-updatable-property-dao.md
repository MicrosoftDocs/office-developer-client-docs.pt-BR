---
title: Propriedade QueryDef.Updatable (DAO)
TOCTitle: Updatable Property
ms:assetid: 9b978b7d-1d76-ff27-a032-dd94660fb088
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198056(v=office.15)
ms:contentKeyID: 48546575
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b0c1a85029270641a944d822ee81954ca1f2528e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919805"
---
# <a name="querydefupdatable-property-dao"></a><span data-ttu-id="9d0c7-102">Propriedade QueryDef.Updatable (DAO)</span><span class="sxs-lookup"><span data-stu-id="9d0c7-102">QueryDef.Updatable property (DAO)</span></span>


<span data-ttu-id="9d0c7-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="9d0c7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9d0c7-p101">Retorna um valor que indica se você pode alterar um objeto DAO. **Boolean** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="9d0c7-p101">Returns a value that indicates whether you can change a DAO object. Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d0c7-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9d0c7-106">Syntax</span></span>

<span data-ttu-id="9d0c7-107">*expressão* . Atualizável</span><span class="sxs-lookup"><span data-stu-id="9d0c7-107">*expression* .Updatable</span></span>

<span data-ttu-id="9d0c7-108">*expressão* Uma variável que representa um objeto **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="9d0c7-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d0c7-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="9d0c7-109">Remarks</span></span>

<span data-ttu-id="9d0c7-110">A propriedade **Updatable** de um objeto **QueryDef** será definida como **True** se a definição da consulta puder ser atualizada, mesmo que o objeto **[Recordset](recordset-object-dao.md)** resultante não seja atualizável.</span><span class="sxs-lookup"><span data-stu-id="9d0c7-110">The **Updatable** property of a **QueryDef** object is set to **True** if the query definition can be updated, even if the resulting **[Recordset](recordset-object-dao.md)** object isn't updatable.</span></span>

