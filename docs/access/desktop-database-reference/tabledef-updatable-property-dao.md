---
title: Propriedade TableDef.Updatable (DAO)
TOCTitle: Updatable Property
ms:assetid: 0b1ae7e5-416d-06f0-5d74-989c6db67ff2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845128(v=office.15)
ms:contentKeyID: 48543168
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 71202203588182ba2bf1ba1449f2b1ee04c82c67
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926196"
---
# <a name="tabledefupdatable-property-dao"></a><span data-ttu-id="fe707-102">Propriedade TableDef.Updatable (DAO)</span><span class="sxs-lookup"><span data-stu-id="fe707-102">TableDef.Updatable property (DAO)</span></span>


<span data-ttu-id="fe707-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="fe707-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fe707-p101">Retorna um valor que indica se você pode alterar um objeto DAO. **Boolean** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="fe707-p101">Returns a value that indicates whether you can change a DAO object. Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe707-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fe707-106">Syntax</span></span>

<span data-ttu-id="fe707-107">*expressão* . Atualizável</span><span class="sxs-lookup"><span data-stu-id="fe707-107">*expression* .Updatable</span></span>

<span data-ttu-id="fe707-108">*expressão* Uma variável que representa um objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="fe707-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe707-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe707-109">Remarks</span></span>

<span data-ttu-id="fe707-p102">A definição da propriedade **Updatable** será sempre **True** para um objeto **TableDef** recentemente criado e **False** para um objeto **TableDef** vinculado. Um novo objeto **TableDef** pode ser acrescentado somente a um banco de dados para o qual o usuário atual tiver permissão de gravação.</span><span class="sxs-lookup"><span data-stu-id="fe707-p102">The **Updatable** property setting is always **True** for a newly created **TableDef** object and **False** for a linked **TableDef** object. A new **TableDef** object can be appended only to a database for which the current user has write permission.</span></span>

