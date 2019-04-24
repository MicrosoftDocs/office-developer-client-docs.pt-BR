---
title: Arquitetura do Outlook PIA
TOCTitle: Architecture of the Outlook PIA
ms:assetid: 89577d14-e6e2-4270-8e72-b0adba378667
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb646255(v=office.15)
ms:contentKeyID: 55119777
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 37ecad42b08b96d79d96d62f98e27913a0309971
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336523"
---
# <a name="architecture-of-the-outlook-pia"></a><span data-ttu-id="8d44f-102">Arquitetura do Outlook PIA</span><span class="sxs-lookup"><span data-stu-id="8d44f-102">Architecture of the Outlook PIA</span></span>

<span data-ttu-id="8d44f-103">O Outlook Primary Interop Assembly (PIA) oferece suporte total ao desenvolvimento em relação ao modelo de objeto do Outlook no código gerenciado.</span><span class="sxs-lookup"><span data-stu-id="8d44f-103">The Outlook Primary Interop Assembly (PIA) fully supports developing against the Outlook object model in managed code.</span></span> <span data-ttu-id="8d44f-104">No entanto, quando você observa o PIA em um navegador de objetos pela primeira vez, pode se surpreender com as muitas interfaces extras que o PIA contém e com o fato de que nem todos os membros de método, propriedade e evento de um objeto são expostos pela mesma interface de objeto.</span><span class="sxs-lookup"><span data-stu-id="8d44f-104">However, when you look at the PIA in an object browser for the first time, you may be surprised by the many extra interfaces that the PIA contains, and the fact that not all method, property, and event members of an object are exposed by the same object interface.</span></span> <span data-ttu-id="8d44f-105">Os tópicos nesta seção descrevem as diretrizes de como acessar os membros do objeto no código e onde procurar ajuda para objetos, métodos, propriedades e eventos.</span><span class="sxs-lookup"><span data-stu-id="8d44f-105">The topics in this section describe guidelines for how to access object members in code, and where to look for help for objects, methods, properties, and events.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8d44f-106">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="8d44f-106">In this section</span></span>

|<span data-ttu-id="8d44f-107">Tópico</span><span class="sxs-lookup"><span data-stu-id="8d44f-107">Topic</span></span>|<span data-ttu-id="8d44f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="8d44f-108">Description</span></span>|
|:----|:----------|
|[<span data-ttu-id="8d44f-109">Associar o Outlook PIA ao modelo de objeto</span><span class="sxs-lookup"><span data-stu-id="8d44f-109">Relating the Outlook PIA with the object model</span></span>](relating-the-outlook-pia-with-the-object-model.md) |<span data-ttu-id="8d44f-110">Fornece uma visão geral de como os objetos e membros no modelo de objeto do Outlook baseado em COM são mapeados para as interfaces e classes gerenciadas correspondentes na PIA.</span><span class="sxs-lookup"><span data-stu-id="8d44f-110">Describes how objects and members in the COM-based Outlook object model are mapped to corresponding managed interfaces and classes in the PIA.</span></span>|
|[<span data-ttu-id="8d44f-111">Objetos no Outlook PIA</span><span class="sxs-lookup"><span data-stu-id="8d44f-111">Objects in the Outlook PIA</span></span>](objects-in-the-outlook-pia.md) |<span data-ttu-id="8d44f-112">Lista as interfaces, classes e delegados .NET que são mapeados para um objeto COM e descreve como acessar um objeto no PIA.</span><span class="sxs-lookup"><span data-stu-id="8d44f-112">Describes the typical .NET interfaces, classes, and delegates that are mapped to a COM object, and describes how to access an object in the PIA.</span></span>|
|[<span data-ttu-id="8d44f-113">Métodos e propriedade no Outlook PIA</span><span class="sxs-lookup"><span data-stu-id="8d44f-113">Methods and properties in the Outlook PIA</span></span>](methods-and-properties-in-the-outlook-pia.md) |<span data-ttu-id="8d44f-114">Descreve como acessar métodos e propriedades de um objeto em código gerenciado usando o PIA.</span><span class="sxs-lookup"><span data-stu-id="8d44f-114">Describes how to access methods and properties of an object in managed code by using the PIA.</span></span>|
|[<span data-ttu-id="8d44f-115">Eventos no Outlook PIA</span><span class="sxs-lookup"><span data-stu-id="8d44f-115">Events in the Outlook PIA</span></span>](events-in-the-outlook-pia.md) |<span data-ttu-id="8d44f-116">Descreve interfaces relacionadas a eventos, delegados e classes auxiliares de coletor no PIA.</span><span class="sxs-lookup"><span data-stu-id="8d44f-116">Describes event-related interfaces, delegates, and sink helper classes in the PIA.</span></span>|

## <a name="see-also"></a><span data-ttu-id="8d44f-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="8d44f-117">See also</span></span>

- [<span data-ttu-id="8d44f-118">Como realizar a configuração para usar o Outlook PIA</span><span class="sxs-lookup"><span data-stu-id="8d44f-118">Setting up to use the Outlook PIA</span></span>](setting-up-to-use-the-outlook-pia.md)
- [<span data-ttu-id="8d44f-119">Desenvolvimento de suplementos gerenciados do Outlook usando o Outlook PIA</span><span class="sxs-lookup"><span data-stu-id="8d44f-119">Developing managed Outlook add-ins using the Outlook PIA</span></span>](developing-managed-outlook-add-ins-using-the-outlook-pia.md)
- [<span data-ttu-id="8d44f-120">Como faço para... (Referência do PIA do Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="8d44f-120">How do I... (Outlook 2013 PIA Reference)</span></span>](how-do-i-outlook-2013-pia-reference.md)

