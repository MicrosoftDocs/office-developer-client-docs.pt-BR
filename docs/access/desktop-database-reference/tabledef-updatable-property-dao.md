---
title: Propriedade TableDef.Updatable (DAO)
TOCTitle: Updatable Property
ms:assetid: 0b1ae7e5-416d-06f0-5d74-989c6db67ff2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845128(v=office.15)
ms:contentKeyID: 48543168
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a6e6c7409b89058c6be55d9fb83eb85c7af9fb9c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28725970"
---
# <a name="tabledefupdatable-property-dao"></a><span data-ttu-id="e1269-102">Propriedade TableDef.Updatable (DAO)</span><span class="sxs-lookup"><span data-stu-id="e1269-102">TableDef.Updatable property (DAO)</span></span>


<span data-ttu-id="e1269-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="e1269-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e1269-p101">Retorna um valor que indica se você pode alterar um objeto DAO. **Boolean** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="e1269-p101">Returns a value that indicates whether you can change a DAO object. Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1269-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e1269-106">Syntax</span></span>

<span data-ttu-id="e1269-107">*expressão* . Atualizável</span><span class="sxs-lookup"><span data-stu-id="e1269-107">*expression* .Updatable</span></span>

<span data-ttu-id="e1269-108">*expressão* Uma variável que representa um objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="e1269-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1269-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="e1269-109">Remarks</span></span>

<span data-ttu-id="e1269-p102">A definição da propriedade **Updatable** será sempre **True** para um objeto **TableDef** recentemente criado e **False** para um objeto **TableDef** vinculado. Um novo objeto **TableDef** pode ser acrescentado somente a um banco de dados para o qual o usuário atual tiver permissão de gravação.</span><span class="sxs-lookup"><span data-stu-id="e1269-p102">The **Updatable** property setting is always **True** for a newly created **TableDef** object and **False** for a linked **TableDef** object. A new **TableDef** object can be appended only to a database for which the current user has write permission.</span></span>

