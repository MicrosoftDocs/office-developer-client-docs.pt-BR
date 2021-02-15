---
title: Evento onError (RDS)
TOCTitle: onError event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9fc51522d143306d9625cdc07251edfe1dddf22d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288473"
---
# <a name="onerror-event-rds"></a><span data-ttu-id="db40e-102">Evento onError (RDS)</span><span class="sxs-lookup"><span data-stu-id="db40e-102">onError event (RDS)</span></span>

<span data-ttu-id="db40e-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="db40e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="db40e-104">O evento **onError** é chamado sempre que ocorre um erro durante uma operação.</span><span class="sxs-lookup"><span data-stu-id="db40e-104">The **onError** event is called whenever an error occurs during an operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="db40e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db40e-105">Syntax</span></span>

<span data-ttu-id="db40e-106">onError *SCode*, *Description*, *Source*, *CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="db40e-106">onError *SCode*, *Description*, *Source*, *CancelDisplay*</span></span>

## <a name="parameters"></a><span data-ttu-id="db40e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db40e-107">Parameters</span></span>

|<span data-ttu-id="db40e-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="db40e-108">Parameter</span></span>|<span data-ttu-id="db40e-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="db40e-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="db40e-110">*SCode*</span><span class="sxs-lookup"><span data-stu-id="db40e-110">*SCode*</span></span> |<span data-ttu-id="db40e-111">Um número inteiro que indica o código de status do erro.</span><span class="sxs-lookup"><span data-stu-id="db40e-111">An integer that indicates the status code of the error.</span></span>|
|<span data-ttu-id="db40e-112">*Description*</span><span class="sxs-lookup"><span data-stu-id="db40e-112">*Description*</span></span> |<span data-ttu-id="db40e-113">Uma **Sequência** que indica uma descrição do erro.</span><span class="sxs-lookup"><span data-stu-id="db40e-113">A **String** that indicates a description of the error.</span></span>|
|<span data-ttu-id="db40e-114">*Source*</span><span class="sxs-lookup"><span data-stu-id="db40e-114">*Source*</span></span> |<span data-ttu-id="db40e-115">Uma **Sequência** que indica a consulta ou o comando que causou o erro.</span><span class="sxs-lookup"><span data-stu-id="db40e-115">A **String** that indicates the query or command that caused the error.</span></span>|
|<span data-ttu-id="db40e-116">*CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="db40e-116">*CancelDisplay*</span></span> |<span data-ttu-id="db40e-117">Um valor **booleano**, que, se for definido como **Verdadeiro**, impede que o erro seja exibido em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="db40e-117">A **Boolean** value, which if set to **True**, that prevents the error from being displayed in a dialog box.</span></span>|

