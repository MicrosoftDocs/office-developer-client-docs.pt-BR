---
title: Eventos ConnectComplete e Disconnect (ADO)
TOCTitle: ConnectComplete and Disconnect events (ADO)
ms:assetid: 8ecb080b-7fc9-7565-25bd-bd57b983750d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249629(v=office.15)
ms:contentKeyID: 48546293
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3ab98e270fd52d656bf722c7f666afbe22d5ea44
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926301"
---
# <a name="connectcomplete-and-disconnect-events-ado"></a><span data-ttu-id="f66ea-102">Eventos ConnectComplete e Disconnect (ADO)</span><span class="sxs-lookup"><span data-stu-id="f66ea-102">ConnectComplete and Disconnect events (ADO)</span></span>


<span data-ttu-id="f66ea-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="f66ea-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f66ea-p101">O evento **ConnectComplete** é chamado após o *início* de uma conexão. O evento **Disconnect** é chamado depois do *término* de uma conexão.</span><span class="sxs-lookup"><span data-stu-id="f66ea-p101">The **ConnectComplete** event is called after a connection *starts*. The **Disconnect** event is called after a connection *ends*.</span></span>

## <a name="syntax"></a><span data-ttu-id="f66ea-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f66ea-106">Syntax</span></span>

<span data-ttu-id="f66ea-107">ConnectComplete*pError*, *adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="f66ea-107">ConnectComplete*pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="f66ea-108">Desconectar*adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="f66ea-108">Disconnect*adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="f66ea-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f66ea-109">Parameters</span></span>

  - <span data-ttu-id="f66ea-110">*pError*</span><span class="sxs-lookup"><span data-stu-id="f66ea-110">*pError*</span></span>

  - <span data-ttu-id="f66ea-p102">Um objeto [Error](error-object-ado.md). Descreve o erro ocorrido se o valor de *adStatus* for **adStatusErrorsOccurred**; caso contrário, não será definido.</span><span class="sxs-lookup"><span data-stu-id="f66ea-p102">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="f66ea-113">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="f66ea-113">*adStatus*</span></span>

  - [<span data-ttu-id="f66ea-114">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="f66ea-114">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="f66ea-115">Quando **ConnectComplete** é chamado, este parâmetro é definido como **adStatusCancel** se um evento **WillConnect** solicitou o cancelamento da conexão pendente.</span><span class="sxs-lookup"><span data-stu-id="f66ea-115">When **ConnectComplete** is called, this parameter is set to **adStatusCancel** if a **WillConnect** event has requested cancellation of the pending connection.</span></span>
    
    <span data-ttu-id="f66ea-p103">Antes do evento retornar, defina este parâmetro como **adStatusUnwantedEvent** para evitar notificações subsequentes. Contudo, o fechamento e a reabertura de [Connection](connection-object-ado.md) faz com que esses eventos ocorram novamente.</span><span class="sxs-lookup"><span data-stu-id="f66ea-p103">Before either event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications. However, closing and reopening the [Connection](connection-object-ado.md) causes these events to occur again.</span></span>

  - <span data-ttu-id="f66ea-118">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="f66ea-118">*pConnection*</span></span>

  - <span data-ttu-id="f66ea-119">O objeto **Connection** ao qual este evento se aplica.</span><span class="sxs-lookup"><span data-stu-id="f66ea-119">The **Connection** object for which this event applies.</span></span>

