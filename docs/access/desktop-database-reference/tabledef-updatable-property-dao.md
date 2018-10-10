---
title: Propriedade TableDef.Updatable (DAO)
TOCTitle: Updatable Property
ms:assetid: 0b1ae7e5-416d-06f0-5d74-989c6db67ff2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845128(v=office.15)
ms:contentKeyID: 48543168
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 44f24e68b60f69304a167d2b9b5ce0b4b0e69b11
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465300"
---
# <a name="tabledefupdatable-property-dao"></a><span data-ttu-id="b14ea-102">Propriedade TableDef.Updatable (DAO)</span><span class="sxs-lookup"><span data-stu-id="b14ea-102">TableDef.Updatable Property (DAO)</span></span>


<span data-ttu-id="b14ea-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b14ea-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b14ea-p101">Retorna um valor que indica se você pode alterar um objeto DAO. **Boolean** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="b14ea-p101">Returns a value that indicates whether you can change a DAO object. Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b14ea-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b14ea-106">Syntax</span></span>

<span data-ttu-id="b14ea-107">*expressão* . Atualizável</span><span class="sxs-lookup"><span data-stu-id="b14ea-107">*expression* .Updatable</span></span>

<span data-ttu-id="b14ea-108">*expressão* Uma variável que representa um objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="b14ea-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b14ea-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="b14ea-109">Remarks</span></span>

<span data-ttu-id="b14ea-p102">A definição da propriedade **Updatable** será sempre **True** para um objeto **TableDef** recentemente criado e **False** para um objeto **TableDef** vinculado. Um novo objeto **TableDef** pode ser acrescentado somente a um banco de dados para o qual o usuário atual tiver permissão de gravação.</span><span class="sxs-lookup"><span data-stu-id="b14ea-p102">The **Updatable** property setting is always **True** for a newly created **TableDef** object and **False** for a linked **TableDef** object. A new **TableDef** object can be appended only to a database for which the current user has write permission.</span></span>

