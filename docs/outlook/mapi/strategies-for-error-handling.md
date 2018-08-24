---
title: Estratégias para lidar com erros
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: be941efd-04b3-48d0-9b9c-8195ad2bb58d
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: b0ec3ada71a3e604ea71c5d386f1ff0466132081
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594086"
---
# <a name="strategies-for-error-handling"></a><span data-ttu-id="13dbd-103">Estratégias para lidar com erros</span><span class="sxs-lookup"><span data-stu-id="13dbd-103">Strategies for Error Handling</span></span>

  
  
<span data-ttu-id="13dbd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13dbd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13dbd-105">Como os métodos de interface são virtuais, não é possível saber, como um chamador, o conjunto completo de valores que pode ser retornado de qualquer uma chamada.</span><span class="sxs-lookup"><span data-stu-id="13dbd-105">Because interface methods are virtual, it is not possible to know, as a caller, the full set of values that can be returned from any one call.</span></span> <span data-ttu-id="13dbd-106">Uma implementação de um método pode retornar cinco valores; outro pode retornar oito.</span><span class="sxs-lookup"><span data-stu-id="13dbd-106">One implementation of a method might return five values; another might return eight.</span></span> <span data-ttu-id="13dbd-107">As entradas de referência na documentação de MAPI listam alguns valores que podem ser retornadas para cada método; Estes são os valores que seu provedor de cliente ou serviço pode procurar e manipular porque eles têm um significado especial.</span><span class="sxs-lookup"><span data-stu-id="13dbd-107">The reference entries in the MAPI documentation list a few values that can be returned for each method; these are the values that your client or service provider can check for and handle because they have special meanings.</span></span> <span data-ttu-id="13dbd-108">Outros valores podem ser retornados, mas porque eles não são significativos, código especial para lidar com aqueles não é necessário.</span><span class="sxs-lookup"><span data-stu-id="13dbd-108">Other values can be returned, but because they are not meaningful, special code to handle those is not necessary.</span></span> <span data-ttu-id="13dbd-109">Uma verificação simple para o sucesso ou falha é adequada.</span><span class="sxs-lookup"><span data-stu-id="13dbd-109">A simple check for success or failure is adequate.</span></span>
  
<span data-ttu-id="13dbd-110">Alguns métodos da interface retornam avisos.</span><span class="sxs-lookup"><span data-stu-id="13dbd-110">A few of the interface methods return warnings.</span></span> <span data-ttu-id="13dbd-111">Se um método que chama o provedor de cliente ou serviço pode retornar um aviso, use a macro **HR_FAILED** para testar o valor de retorno em vez de uma verificação para zero ou diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="13dbd-111">If a method that your client or service provider calls can return a warning, use the **HR_FAILED** macro to test the return value rather than a check for zero or nonzero.</span></span> <span data-ttu-id="13dbd-112">Avisos, embora diferente de zero, diferem dos códigos de erro em que não têm alto estará definido o bit definido.</span><span class="sxs-lookup"><span data-stu-id="13dbd-112">Warnings, although nonzero, differ from error codes in that they do not have the high bit set.</span></span> <span data-ttu-id="13dbd-113">Se seu provedor de cliente ou serviço não usar a macro, é provável que um aviso pode ser errado para uma falha.</span><span class="sxs-lookup"><span data-stu-id="13dbd-113">If your client or service provider does not use the macro, it is likely that a warning might be mistaken for a failure.</span></span> 
  
<span data-ttu-id="13dbd-114">Embora a maioria dos métodos de interface e funções retornam valores HRESULT, algumas funções retornam valores longos não assinados.</span><span class="sxs-lookup"><span data-stu-id="13dbd-114">Although most interface methods and functions return HRESULT values, some functions return unsigned long values.</span></span> <span data-ttu-id="13dbd-115">Além disso, alguns métodos usados no ambiente de MAPI COM são provenientes e retornam valores de erro COM em vez de valores de erro MAPI.</span><span class="sxs-lookup"><span data-stu-id="13dbd-115">Also, some methods used in the MAPI environment come from COM and return COM error values rather than MAPI error values.</span></span> <span data-ttu-id="13dbd-116">Tenha em mente as seguintes diretrizes ao fazer chamadas:</span><span class="sxs-lookup"><span data-stu-id="13dbd-116">Keep in mind the following guidelines when making calls:</span></span>
  
- <span data-ttu-id="13dbd-117">Nunca dependa ou usar os valores de retorno de **AddRef** ou **IUnknown:: Release**.</span><span class="sxs-lookup"><span data-stu-id="13dbd-117">Never rely on or use the return values from **IUnknown::AddRef** or **IUnknown::Release**.</span></span> <span data-ttu-id="13dbd-118">Esses valores de retorno são para fins de diagnóstico apenas.</span><span class="sxs-lookup"><span data-stu-id="13dbd-118">These return values are for diagnostic purposes only.</span></span> 
    
- <span data-ttu-id="13dbd-119">**IUnknown:: QueryInterface** sempre retorna erros COM genéricos, onde o recurso é FACILITY_NULL ou FACILITY_RPC, em vez de erros MAPI.</span><span class="sxs-lookup"><span data-stu-id="13dbd-119">**IUnknown::QueryInterface** always returns generic COM errors where the facility is FACILITY_NULL or FACILITY_RPC, rather than MAPI errors.</span></span> 
    
- <span data-ttu-id="13dbd-120">Todos os outros métodos de interface retornam erros de interface MAPI com um recurso de FACILITY_ITF ou FACILITY_RPC ou FACILITY_NULL.</span><span class="sxs-lookup"><span data-stu-id="13dbd-120">All other interface methods return MAPI interface errors with a facility of FACILITY_ITF, or FACILITY_RPC or FACILITY_NULL errors.</span></span>
    
<span data-ttu-id="13dbd-121">Quando uma chamada for feita para um método de MAPI sem suporte, uma das quatro possíveis erros pode ser retornada:</span><span class="sxs-lookup"><span data-stu-id="13dbd-121">When a call is made to an unsupported MAPI method, one of four possible errors can be returned:</span></span> 
  
<span data-ttu-id="13dbd-122">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="13dbd-122">MAPI_E_NO_SUPPORT</span></span>
  
<span data-ttu-id="13dbd-123">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="13dbd-123">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span>
  
<span data-ttu-id="13dbd-124">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="13dbd-124">MAPI_E_INVALID_PARAMETER</span></span>
  
<span data-ttu-id="13dbd-125">MAPI_E_VERSION.</span><span class="sxs-lookup"><span data-stu-id="13dbd-125">MAPI_E_VERSION.</span></span> 
  

