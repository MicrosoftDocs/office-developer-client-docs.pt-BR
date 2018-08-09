---
title: Função QUEUEMARKEREVENT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60107
localization_priority: Normal
ms.assetid: b4671715-4209-7774-c174-c19dc9721a02
description: Faz com que o aplicativo emita um evento de marcador no seu complemento, o Microsoft Visual Basic for Applications (VBA) código ou suplemento COM.
ms.openlocfilehash: b9175caf0845530c93f6db15e286f3eae21ea415
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772626"
---
# <a name="queuemarkerevent-function"></a><span data-ttu-id="fe85b-103">Função QUEUEMARKEREVENT</span><span class="sxs-lookup"><span data-stu-id="fe85b-103">QUEUEMARKEREVENT Function</span></span>

<span data-ttu-id="fe85b-104">Faz com que o aplicativo emita um evento de marcador no seu complemento, o Microsoft Visual Basic for Applications (VBA) código ou suplemento COM.</span><span class="sxs-lookup"><span data-stu-id="fe85b-104">Causes the application to fire a marker event to your add-on, Microsoft Visual Basic for Applications (VBA) code, or COM add-in.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="fe85b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fe85b-105">Syntax</span></span>

<span data-ttu-id="fe85b-106">QUEUEMARKEREVENT (* * *event_string* * *)</span><span class="sxs-lookup"><span data-stu-id="fe85b-106">QUEUEMARKEREVENT (** *event_string* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="fe85b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fe85b-107">Parameters</span></span>

|<span data-ttu-id="fe85b-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="fe85b-108">**Name**</span></span>|<span data-ttu-id="fe85b-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="fe85b-109">**Required/Optional**</span></span>|<span data-ttu-id="fe85b-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="fe85b-110">**Data Type**</span></span>|<span data-ttu-id="fe85b-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fe85b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="fe85b-112">_event_string_</span><span class="sxs-lookup"><span data-stu-id="fe85b-112">_event_string_</span></span> <br/> |<span data-ttu-id="fe85b-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="fe85b-113">Required</span></span>  <br/> |<span data-ttu-id="fe85b-114">**String**</span><span class="sxs-lookup"><span data-stu-id="fe85b-114">**String**</span></span> <br/> | <span data-ttu-id="fe85b-115">A cadeia de caracteres a serem passados para o manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="fe85b-115">The string to pass to your event handler.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fe85b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe85b-116">Remarks</span></span>

<span data-ttu-id="fe85b-117">A função QUEUEMARKEREVENT fornece aos desenvolvedores uma maneira para notificar o código de uma célula ShapeSheet e passar informações específicas da solução.</span><span class="sxs-lookup"><span data-stu-id="fe85b-117">The QUEUEMARKEREVENT function provides developers with a way to notify their code from a ShapeSheet cell, and pass solution-specific information.</span></span> <span data-ttu-id="fe85b-118">Quando a célula que contém a fórmula com a função QUEUEMARKEREVENT é avaliada, o aplicativo dispara um evento de marcador e passa _event_string_ para todos os manipuladores de eventos que estejam escutando o evento **MarkerEvent** .</span><span class="sxs-lookup"><span data-stu-id="fe85b-118">When the cell containing the formula with the QUEUEMARKEREVENT function is evaluated, the application fires a marker event and passes  _event_string_ to all event handlers that are listening to the **MarkerEvent** event.</span></span> 
  
<span data-ttu-id="fe85b-119">Para obter mais informações sobre eventos de marcadores, consulte o método **QueueMarkerEvent** e o **evento MarkerEvent na referência de automação do Microsoft Visio** .</span><span class="sxs-lookup"><span data-stu-id="fe85b-119">For more information about marker events, see the **QueueMarkerEvent** method and **MarkerEvent** event topics in the Microsoft Visio Automation Reference.</span></span> 
  
## <a name="example"></a><span data-ttu-id="fe85b-120">Exemplo</span><span class="sxs-lookup"><span data-stu-id="fe85b-120">Example</span></span>

<span data-ttu-id="fe85b-121">QUEUEMARKEREVENT ("MinhaNotificaçãoPersonalizada")</span><span class="sxs-lookup"><span data-stu-id="fe85b-121">QUEUEMARKEREVENT ("MyCustomNotification")</span></span> 
  
<span data-ttu-id="fe85b-122">Faz com que o aplicativo emita um evento de marcador e passe a sequência de caracteres "MinhaNotificaçãoPersonalizada" para manipuladores de eventos que estejam escutando o evento **MarkerEvent**.</span><span class="sxs-lookup"><span data-stu-id="fe85b-122">Causes the application to fire a marker event, and passes the string "MyCustomNotification" to event handlers that are listening to the **MarkerEvent** event.</span></span> 
  

