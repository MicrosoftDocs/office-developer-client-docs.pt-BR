---
title: Evento onError (RDS)
TOCTitle: onError Event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3fe6f6b78297008e25e15dc17e243ae982a5ccf3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465085"
---
# <a name="onerror-event-rds"></a><span data-ttu-id="a5a46-102">Evento onError (RDS)</span><span class="sxs-lookup"><span data-stu-id="a5a46-102">onError Event (RDS)</span></span>


<span data-ttu-id="a5a46-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a5a46-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a5a46-104">O evento **onError** é chamado sempre que ocorre um erro durante uma operação.</span><span class="sxs-lookup"><span data-stu-id="a5a46-104">The **onError** event is called whenever an error occurs during an operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5a46-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a5a46-105">Syntax</span></span>

<span data-ttu-id="a5a46-106">AoOcorrerErro*SCode*, *Descrição*, *fonte*, *CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="a5a46-106">onError*SCode*, *Description*, *Source*, *CancelDisplay*</span></span>

## <a name="parameters"></a><span data-ttu-id="a5a46-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a5a46-107">Parameters</span></span>

  - <span data-ttu-id="a5a46-108">*SCode*</span><span class="sxs-lookup"><span data-stu-id="a5a46-108">*SCode*</span></span>

  - <span data-ttu-id="a5a46-109">Um número inteiro que indica o código de status do erro.</span><span class="sxs-lookup"><span data-stu-id="a5a46-109">An integer that indicates the status code of the error.</span></span>

  - <span data-ttu-id="a5a46-110">*Description*</span><span class="sxs-lookup"><span data-stu-id="a5a46-110">*Description*</span></span>

  - <span data-ttu-id="a5a46-111">Uma **Sequência** que indica uma descrição do erro.</span><span class="sxs-lookup"><span data-stu-id="a5a46-111">A **String** that indicates a description of the error.</span></span>

  - <span data-ttu-id="a5a46-112">*Source*</span><span class="sxs-lookup"><span data-stu-id="a5a46-112">*Source*</span></span>

  - <span data-ttu-id="a5a46-113">Uma **Sequência** que indica a consulta ou o comando que causou o erro.</span><span class="sxs-lookup"><span data-stu-id="a5a46-113">A **String** that indicates the query or command that caused the error.</span></span>

  - <span data-ttu-id="a5a46-114">*CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="a5a46-114">*CancelDisplay*</span></span>

  - <span data-ttu-id="a5a46-115">Um valor **booleano**, que, se for definido como **Verdadeiro**, impede que o erro seja exibido em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="a5a46-115">A **Boolean** value, which if set to **True**, that prevents the error from being displayed in a dialog box.</span></span>

