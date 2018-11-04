---
title: Eventos ConnectComplete e Disconnect (ADO)
TOCTitle: ConnectComplete and Disconnect events (ADO)
ms:assetid: 8ecb080b-7fc9-7565-25bd-bd57b983750d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249629(v=office.15)
ms:contentKeyID: 48546293
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f49bbffc2cfbaec77bf1b0d6aa692412c45254ae
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949678"
---
# <a name="connectcomplete-and-disconnect-events-ado"></a><span data-ttu-id="186a6-102">Eventos ConnectComplete e Disconnect (ADO)</span><span class="sxs-lookup"><span data-stu-id="186a6-102">ConnectComplete and Disconnect events (ADO)</span></span>

<span data-ttu-id="186a6-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="186a6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="186a6-p101">O evento **ConnectComplete** é chamado após o *início* de uma conexão. O evento **Disconnect** é chamado depois do *término* de uma conexão.</span><span class="sxs-lookup"><span data-stu-id="186a6-p101">The **ConnectComplete** event is called after a connection *starts*. The **Disconnect** event is called after a connection *ends*.</span></span>

## <a name="syntax"></a><span data-ttu-id="186a6-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="186a6-106">Syntax</span></span>

<span data-ttu-id="186a6-107">ConnectComplete*pError*, *adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="186a6-107">ConnectComplete*pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="186a6-108">Desconectar*adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="186a6-108">Disconnect*adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="186a6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="186a6-109">Parameters</span></span>

|<span data-ttu-id="186a6-110">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="186a6-110">Parameter</span></span>|<span data-ttu-id="186a6-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="186a6-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="186a6-112">*pError*</span><span class="sxs-lookup"><span data-stu-id="186a6-112">*pError*</span></span> |<span data-ttu-id="186a6-p102">Um objeto [Error](error-object-ado.md). Descreve o erro ocorrido se o valor de *adStatus* for **adStatusErrorsOccurred**; caso contrário, não será definido.</span><span class="sxs-lookup"><span data-stu-id="186a6-p102">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="186a6-115">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="186a6-115">*adStatus*</span></span> |<span data-ttu-id="186a6-116">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="186a6-116">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="186a6-117">Quando **ConnectComplete** é chamado, este parâmetro é definido como **adStatusCancel** se um evento **WillConnect** solicitou o cancelamento da conexão pendente.</span><span class="sxs-lookup"><span data-stu-id="186a6-117">When **ConnectComplete** is called, this parameter is set to **adStatusCancel** if a **WillConnect** event has requested cancellation of the pending connection.</span></span><br/><br/><span data-ttu-id="186a6-p104">Antes do evento retornar, defina este parâmetro como **adStatusUnwantedEvent** para evitar notificações subsequentes. Contudo, o fechamento e a reabertura de [Connection](connection-object-ado.md) faz com que esses eventos ocorram novamente.</span><span class="sxs-lookup"><span data-stu-id="186a6-p104">Before either event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications. However, closing and reopening the [Connection](connection-object-ado.md) causes these events to occur again.</span></span>|
|<span data-ttu-id="186a6-120">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="186a6-120">*pConnection*</span></span> |<span data-ttu-id="186a6-121">O objeto **Connection** ao qual este evento se aplica.</span><span class="sxs-lookup"><span data-stu-id="186a6-121">The **Connection** object for which this event applies.</span></span>|

