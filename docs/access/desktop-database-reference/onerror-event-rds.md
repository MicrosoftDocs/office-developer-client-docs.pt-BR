---
title: Evento onError (RDS)
TOCTitle: onError event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a61ec584f5baddcfdb8ce1f6dda1bf990546c053
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949352"
---
# <a name="onerror-event-rds"></a><span data-ttu-id="407cf-102">Evento onError (RDS)</span><span class="sxs-lookup"><span data-stu-id="407cf-102">onError event (RDS)</span></span>

<span data-ttu-id="407cf-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="407cf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="407cf-104">O evento **onError** é chamado sempre que ocorre um erro durante uma operação.</span><span class="sxs-lookup"><span data-stu-id="407cf-104">The **onError** event is called whenever an error occurs during an operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="407cf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="407cf-105">Syntax</span></span>

<span data-ttu-id="407cf-106">AoOcorrerErro*SCode*, *Descrição*, *fonte*, *CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="407cf-106">onError*SCode*, *Description*, *Source*, *CancelDisplay*</span></span>

## <a name="parameters"></a><span data-ttu-id="407cf-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="407cf-107">Parameters</span></span>

|<span data-ttu-id="407cf-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="407cf-108">Parameter</span></span>|<span data-ttu-id="407cf-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="407cf-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="407cf-110">*SCode*</span><span class="sxs-lookup"><span data-stu-id="407cf-110">*SCode*</span></span> |<span data-ttu-id="407cf-111">Um número inteiro que indica o código de status do erro.</span><span class="sxs-lookup"><span data-stu-id="407cf-111">An integer that indicates the status code of the error.</span></span>|
|<span data-ttu-id="407cf-112">*Description*</span><span class="sxs-lookup"><span data-stu-id="407cf-112">*Description*</span></span> |<span data-ttu-id="407cf-113">Uma **Sequência** que indica uma descrição do erro.</span><span class="sxs-lookup"><span data-stu-id="407cf-113">A **String** that indicates a description of the error.</span></span>|
|<span data-ttu-id="407cf-114">*Source*</span><span class="sxs-lookup"><span data-stu-id="407cf-114">*Source*</span></span> |<span data-ttu-id="407cf-115">Uma **Sequência** que indica a consulta ou o comando que causou o erro.</span><span class="sxs-lookup"><span data-stu-id="407cf-115">A **String** that indicates the query or command that caused the error.</span></span>|
|<span data-ttu-id="407cf-116">*CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="407cf-116">*CancelDisplay*</span></span> |<span data-ttu-id="407cf-117">Um valor **booleano**, que, se for definido como **Verdadeiro**, impede que o erro seja exibido em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="407cf-117">A **Boolean** value, which if set to **True**, that prevents the error from being displayed in a dialog box.</span></span>|

