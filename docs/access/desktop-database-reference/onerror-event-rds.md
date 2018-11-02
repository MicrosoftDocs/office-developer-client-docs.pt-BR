---
title: Evento onError (RDS)
TOCTitle: onError event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c67e277c35e3cf6c75226dc138aa4b288843e6bf
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930858"
---
# <a name="onerror-event-rds"></a><span data-ttu-id="9d3e3-102">Evento onError (RDS)</span><span class="sxs-lookup"><span data-stu-id="9d3e3-102">onError event (RDS)</span></span>


<span data-ttu-id="9d3e3-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="9d3e3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9d3e3-104">O evento **onError** é chamado sempre que ocorre um erro durante uma operação.</span><span class="sxs-lookup"><span data-stu-id="9d3e3-104">The **onError** event is called whenever an error occurs during an operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d3e3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9d3e3-105">Syntax</span></span>

<span data-ttu-id="9d3e3-106">AoOcorrerErro*SCode*, *Descrição*, *fonte*, *CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="9d3e3-106">onError*SCode*, *Description*, *Source*, *CancelDisplay*</span></span>

## <a name="parameters"></a><span data-ttu-id="9d3e3-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9d3e3-107">Parameters</span></span>

  - <span data-ttu-id="9d3e3-108">*SCode*</span><span class="sxs-lookup"><span data-stu-id="9d3e3-108">*SCode*</span></span>

  - <span data-ttu-id="9d3e3-109">Um número inteiro que indica o código de status do erro.</span><span class="sxs-lookup"><span data-stu-id="9d3e3-109">An integer that indicates the status code of the error.</span></span>

  - <span data-ttu-id="9d3e3-110">*Description*</span><span class="sxs-lookup"><span data-stu-id="9d3e3-110">*Description*</span></span>

  - <span data-ttu-id="9d3e3-111">Uma **Sequência** que indica uma descrição do erro.</span><span class="sxs-lookup"><span data-stu-id="9d3e3-111">A **String** that indicates a description of the error.</span></span>

  - <span data-ttu-id="9d3e3-112">*Source*</span><span class="sxs-lookup"><span data-stu-id="9d3e3-112">*Source*</span></span>

  - <span data-ttu-id="9d3e3-113">Uma **Sequência** que indica a consulta ou o comando que causou o erro.</span><span class="sxs-lookup"><span data-stu-id="9d3e3-113">A **String** that indicates the query or command that caused the error.</span></span>

  - <span data-ttu-id="9d3e3-114">*CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="9d3e3-114">*CancelDisplay*</span></span>

  - <span data-ttu-id="9d3e3-115">Um valor **booleano**, que, se for definido como **Verdadeiro**, impede que o erro seja exibido em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9d3e3-115">A **Boolean** value, which if set to **True**, that prevents the error from being displayed in a dialog box.</span></span>

