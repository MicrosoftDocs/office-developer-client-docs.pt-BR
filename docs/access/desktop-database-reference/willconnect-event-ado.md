---
title: Evento WillConnect (ADO)
TOCTitle: WillConnect Event (ADO)
ms:assetid: 8b0e9955-4e7a-7af8-ce6c-7a4ba569a5bb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249611(v=office.15)
ms:contentKeyID: 48546208
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c5493593998bf5484bd2247b32e114809b805fda
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465309"
---
# <a name="willconnect-event-ado"></a><span data-ttu-id="5cf4a-102">Evento WillConnect (ADO)</span><span class="sxs-lookup"><span data-stu-id="5cf4a-102">WillConnect Event (ADO)</span></span>


<span data-ttu-id="5cf4a-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5cf4a-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="5cf4a-104">O evento **WillConnect** é chamado antes que uma conexão seja iniciada.</span><span class="sxs-lookup"><span data-stu-id="5cf4a-104">The **WillConnect** event is called before a connection starts.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cf4a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5cf4a-105">Syntax</span></span>

<span data-ttu-id="5cf4a-106">WillConnect*ConnectionString*, *UserID*, *senha*, *Opções*, *adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="5cf4a-106">WillConnect*ConnectionString*, *UserID*, *Password*, *Options*, *adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="5cf4a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5cf4a-107">Parameters</span></span>

  - <span data-ttu-id="5cf4a-108">*ConnectionString*</span><span class="sxs-lookup"><span data-stu-id="5cf4a-108">*ConnectionString*</span></span>

  - <span data-ttu-id="5cf4a-109">Uma **String** que contém informações de conexão para a conexão pendente.</span><span class="sxs-lookup"><span data-stu-id="5cf4a-109">A **String** that contains connection information for the pending connection.</span></span>

  - <span data-ttu-id="5cf4a-110">*UserID*</span><span class="sxs-lookup"><span data-stu-id="5cf4a-110">*UserID*</span></span>

  - <span data-ttu-id="5cf4a-111">Um **String** que contém um nome de usuário para a conexão pendente.</span><span class="sxs-lookup"><span data-stu-id="5cf4a-111">A **String** that contains a user name for the pending connection.</span></span>

  - <span data-ttu-id="5cf4a-112">*Password*</span><span class="sxs-lookup"><span data-stu-id="5cf4a-112">*Password*</span></span>

  - <span data-ttu-id="5cf4a-113">Uma **String** que contém uma senha para a conexão pendente.</span><span class="sxs-lookup"><span data-stu-id="5cf4a-113">A **String** that contains a password for the pending connection.</span></span>

  - <span data-ttu-id="5cf4a-114">*Options*</span><span class="sxs-lookup"><span data-stu-id="5cf4a-114">*Options*</span></span>

  - <span data-ttu-id="5cf4a-p101">Um valor **Long** que indica como o provedor deve avaliar o *ConnectionString*. Sua única opção é **adAsyncOpen**.</span><span class="sxs-lookup"><span data-stu-id="5cf4a-p101">A **Long** value that indicates how the provider should evaluate the *ConnectionString*. Your only option is **adAsyncOpen**.</span></span>

  - <span data-ttu-id="5cf4a-117">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="5cf4a-117">*adStatus*</span></span>

  - [<span data-ttu-id="5cf4a-118">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="5cf4a-118">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="5cf4a-p102">Quando esse evento é chamado, esse parâmetro é definido como **adStatusOK**, por padrão. Ele será definido como **adStatusCantDeny** se o evento não puder solicitar o cancelamento da operação pendente.</span><span class="sxs-lookup"><span data-stu-id="5cf4a-p102">When this event is called, this parameter is set to **adStatusOK** by default. It is set to **adStatusCantDeny** if the event cannot request cancellation of the pending operation.</span></span>
    
    <span data-ttu-id="5cf4a-p103">Antes que esse evento seja retornado, defina esse parâmetro como **adStatusUnwantedEvent** para impedir notificações subsequentes. Defina esse parâmetro como **adStatusCancel** para solicitar uma operação de conexão que provocou o cancelamento dessa notificação.</span><span class="sxs-lookup"><span data-stu-id="5cf4a-p103">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications. Set this parameter to **adStatusCancel** to request the connection operation that caused cancellation of this notification.</span></span>

  - <span data-ttu-id="5cf4a-123">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="5cf4a-123">*pConnection*</span></span>

  - <span data-ttu-id="5cf4a-p104">O objeto [Connection](connection-object-ado.md) ao qual essa notificação de evento se aplica. As alterações aos parâmetros de **Connection** pela manipulador de eventos **WillConnect** não terão efeito no **Connection**.</span><span class="sxs-lookup"><span data-stu-id="5cf4a-p104">The [Connection](connection-object-ado.md) object for which this event notification applies. Changes to the parameters of the **Connection** by the **WillConnect** event handler will have no effect on the **Connection**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5cf4a-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="5cf4a-126">Remarks</span></span>

<span data-ttu-id="5cf4a-p105">Quando o **WillConnect** é chamado, os parâmetros *ConnectionString*, *UserID*, *Password* e *Options* são definidos como os valores estabelecidos pela operação que provocou esse evento (a conexão pendente) e podem ser alterados antes que o evento seja retornado. O **WillConnect** pode retornar uma solicitação para que a conexão pendente seja cancelada.</span><span class="sxs-lookup"><span data-stu-id="5cf4a-p105">When **WillConnect** is called, the *ConnectionString*, *UserID*, *Password*, and *Options* parameters are set to the values established by the operation that caused this event (the pending connection), and can be changed before the event returns. **WillConnect** may return a request that the pending connection be canceled.</span></span>

<span data-ttu-id="5cf4a-129">Quando esse evento for cancelado, **ConnectComplete** será chamado com seu parâmetro *adStatus* definido como **adStatusErrorsOccurred**.</span><span class="sxs-lookup"><span data-stu-id="5cf4a-129">When this event is canceled, **ConnectComplete** will be called with its *adStatus* parameter set to **adStatusErrorsOccurred**.</span></span>

