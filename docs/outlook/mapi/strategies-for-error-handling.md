---
title: Estratégias para tratamento de erros
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: be941efd-04b3-48d0-9b9c-8195ad2bb58d
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: e778df216d0fe9b901cd9f7136c8014a6b8f0d0a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770506"
---
# <a name="strategies-for-error-handling"></a><span data-ttu-id="e79ff-103">Estratégias para tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="e79ff-103">Strategies for Error Handling</span></span>

  
  
<span data-ttu-id="e79ff-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e79ff-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e79ff-105">Como os métodos de interface são virtuais, não é possível saber, como um chamador, o conjunto completo de valores que pode ser retornado de qualquer uma chamada.</span><span class="sxs-lookup"><span data-stu-id="e79ff-105">Because interface methods are virtual, it is not possible to know, as a caller, the full set of values that can be returned from any one call.</span></span> <span data-ttu-id="e79ff-106">Uma implementação de um método pode retornar cinco valores; outro pode retornar oito.</span><span class="sxs-lookup"><span data-stu-id="e79ff-106">One implementation of a method might return five values; another might return eight.</span></span> <span data-ttu-id="e79ff-107">As entradas de referência na documentação de MAPI listam alguns valores que podem ser retornadas para cada método; Estes são os valores que seu provedor de cliente ou serviço pode procurar e manipular porque eles têm um significado especial.</span><span class="sxs-lookup"><span data-stu-id="e79ff-107">The reference entries in the MAPI documentation list a few values that can be returned for each method; these are the values that your client or service provider can check for and handle because they have special meanings.</span></span> <span data-ttu-id="e79ff-108">Outros valores podem ser retornados, mas porque eles não são significativos, código especial para lidar com aqueles não é necessário.</span><span class="sxs-lookup"><span data-stu-id="e79ff-108">Other values can be returned, but because they are not meaningful, special code to handle those is not necessary.</span></span> <span data-ttu-id="e79ff-109">Uma verificação simple para o sucesso ou falha é adequada.</span><span class="sxs-lookup"><span data-stu-id="e79ff-109">A simple check for success or failure is adequate.</span></span>
  
<span data-ttu-id="e79ff-110">Alguns métodos da interface retornam avisos.</span><span class="sxs-lookup"><span data-stu-id="e79ff-110">A few of the interface methods return warnings.</span></span> <span data-ttu-id="e79ff-111">Se um método que chama o provedor de cliente ou serviço pode retornar um aviso, use a macro **HR_FAILED** para testar o valor de retorno em vez de uma verificação para zero ou diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="e79ff-111">If a method that your client or service provider calls can return a warning, use the **HR_FAILED** macro to test the return value rather than a check for zero or nonzero.</span></span> <span data-ttu-id="e79ff-112">Avisos, embora diferente de zero, diferem dos códigos de erro em que não têm alto estará definido o bit definido.</span><span class="sxs-lookup"><span data-stu-id="e79ff-112">Warnings, although nonzero, differ from error codes in that they do not have the high bit set.</span></span> <span data-ttu-id="e79ff-113">Se seu provedor de cliente ou serviço não usar a macro, é provável que um aviso pode ser errado para uma falha.</span><span class="sxs-lookup"><span data-stu-id="e79ff-113">If your client or service provider does not use the macro, it is likely that a warning might be mistaken for a failure.</span></span> 
  
<span data-ttu-id="e79ff-114">Embora a maioria dos métodos de interface e funções retornam valores HRESULT, algumas funções retornam valores longos não assinados.</span><span class="sxs-lookup"><span data-stu-id="e79ff-114">Although most interface methods and functions return HRESULT values, some functions return unsigned long values.</span></span> <span data-ttu-id="e79ff-115">Além disso, alguns métodos usados no ambiente de MAPI COM são provenientes e retornam valores de erro COM em vez de valores de erro MAPI.</span><span class="sxs-lookup"><span data-stu-id="e79ff-115">Also, some methods used in the MAPI environment come from COM and return COM error values rather than MAPI error values.</span></span> <span data-ttu-id="e79ff-116">Tenha em mente as seguintes diretrizes ao fazer chamadas:</span><span class="sxs-lookup"><span data-stu-id="e79ff-116">Keep in mind the following guidelines when making calls:</span></span>
  
- <span data-ttu-id="e79ff-117">Nunca dependa ou usar os valores de retorno de **AddRef** ou **IUnknown:: Release**.</span><span class="sxs-lookup"><span data-stu-id="e79ff-117">Never rely on or use the return values from **IUnknown::AddRef** or **IUnknown::Release**.</span></span> <span data-ttu-id="e79ff-118">Esses valores de retorno são para fins de diagnóstico apenas.</span><span class="sxs-lookup"><span data-stu-id="e79ff-118">These return values are for diagnostic purposes only.</span></span> 
    
- <span data-ttu-id="e79ff-119">**IUnknown:: QueryInterface** sempre retorna erros COM genéricos, onde o recurso é FACILITY_NULL ou FACILITY_RPC, em vez de erros MAPI.</span><span class="sxs-lookup"><span data-stu-id="e79ff-119">**IUnknown::QueryInterface** always returns generic COM errors where the facility is FACILITY_NULL or FACILITY_RPC, rather than MAPI errors.</span></span> 
    
- <span data-ttu-id="e79ff-120">Todos os outros métodos de interface retornam erros de interface MAPI com um recurso de FACILITY_ITF ou FACILITY_RPC ou FACILITY_NULL.</span><span class="sxs-lookup"><span data-stu-id="e79ff-120">All other interface methods return MAPI interface errors with a facility of FACILITY_ITF, or FACILITY_RPC or FACILITY_NULL errors.</span></span>
    
<span data-ttu-id="e79ff-121">Quando uma chamada for feita para um método de MAPI sem suporte, uma das quatro possíveis erros pode ser retornada:</span><span class="sxs-lookup"><span data-stu-id="e79ff-121">When a call is made to an unsupported MAPI method, one of four possible errors can be returned:</span></span> 
  
<span data-ttu-id="e79ff-122">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="e79ff-122">MAPI_E_NO_SUPPORT</span></span>
  
<span data-ttu-id="e79ff-123">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="e79ff-123">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span>
  
<span data-ttu-id="e79ff-124">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e79ff-124">MAPI_E_INVALID_PARAMETER</span></span>
  
<span data-ttu-id="e79ff-125">MAPI_E_VERSION.</span><span class="sxs-lookup"><span data-stu-id="e79ff-125">MAPI_E_VERSION.</span></span> 
  

