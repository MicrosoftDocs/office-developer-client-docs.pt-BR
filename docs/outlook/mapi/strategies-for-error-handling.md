---
title: Estratégias para tratamento de erros
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: be941efd-04b3-48d0-9b9c-8195ad2bb58d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9e76ae3f292d8348b9dc64cb54bffae96b96e871
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424144"
---
# <a name="strategies-for-error-handling"></a><span data-ttu-id="c4faf-103">Estratégias para tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="c4faf-103">Strategies for Error Handling</span></span>

  
  
<span data-ttu-id="c4faf-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c4faf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c4faf-105">Como os métodos de interface são virtuais, não é possível saber, como um chamador, o conjunto completo de valores que podem ser retornados de qualquer uma das chamadas.</span><span class="sxs-lookup"><span data-stu-id="c4faf-105">Because interface methods are virtual, it is not possible to know, as a caller, the full set of values that can be returned from any one call.</span></span> <span data-ttu-id="c4faf-106">Uma implementação de um método pode retornar cinco valores; outra pode retornar oito.</span><span class="sxs-lookup"><span data-stu-id="c4faf-106">One implementation of a method might return five values; another might return eight.</span></span> <span data-ttu-id="c4faf-107">As entradas de referência na lista de documentação MAPI têm alguns valores que podem ser retornados para cada método; Estes são os valores que o cliente ou provedor de serviços pode verificar e lidar porque têm significados especiais.</span><span class="sxs-lookup"><span data-stu-id="c4faf-107">The reference entries in the MAPI documentation list a few values that can be returned for each method; these are the values that your client or service provider can check for and handle because they have special meanings.</span></span> <span data-ttu-id="c4faf-108">Outros valores podem ser retornados, mas por não serem significativos, não é necessário código especial para lidar com eles.</span><span class="sxs-lookup"><span data-stu-id="c4faf-108">Other values can be returned, but because they are not meaningful, special code to handle those is not necessary.</span></span> <span data-ttu-id="c4faf-109">Uma simples verificação de sucesso ou falha é adequada.</span><span class="sxs-lookup"><span data-stu-id="c4faf-109">A simple check for success or failure is adequate.</span></span>
  
<span data-ttu-id="c4faf-110">Alguns métodos de interface retornam avisos.</span><span class="sxs-lookup"><span data-stu-id="c4faf-110">A few of the interface methods return warnings.</span></span> <span data-ttu-id="c4faf-111">Se um método que seu cliente ou provedor de serviços chamar puder retornar um aviso, use a macro **HR_FAILED** para testar o valor de retorno em vez de uma verificação de zero ou zero.</span><span class="sxs-lookup"><span data-stu-id="c4faf-111">If a method that your client or service provider calls can return a warning, use the **HR_FAILED** macro to test the return value rather than a check for zero or nonzero.</span></span> <span data-ttu-id="c4faf-112">Os avisos, embora não nulo, diferem dos códigos de erro, pois eles não têm o conjunto de bits alto.</span><span class="sxs-lookup"><span data-stu-id="c4faf-112">Warnings, although nonzero, differ from error codes in that they do not have the high bit set.</span></span> <span data-ttu-id="c4faf-113">Se o cliente ou provedor de serviços não usar a macro, é provável que um aviso possa ser confundido para uma falha.</span><span class="sxs-lookup"><span data-stu-id="c4faf-113">If your client or service provider does not use the macro, it is likely that a warning might be mistaken for a failure.</span></span> 
  
<span data-ttu-id="c4faf-114">Embora a maioria dos métodos e funções de interface retornem valores HRESULT, algumas funções retornam valores Long não assinados.</span><span class="sxs-lookup"><span data-stu-id="c4faf-114">Although most interface methods and functions return HRESULT values, some functions return unsigned long values.</span></span> <span data-ttu-id="c4faf-115">Além disso, alguns métodos usados no ambiente MAPI são provenientes do COM e retornam valores de erro COM em vez de valores de erro MAPI.</span><span class="sxs-lookup"><span data-stu-id="c4faf-115">Also, some methods used in the MAPI environment come from COM and return COM error values rather than MAPI error values.</span></span> <span data-ttu-id="c4faf-116">Tenha em mente as seguintes diretrizes ao fazer chamadas:</span><span class="sxs-lookup"><span data-stu-id="c4faf-116">Keep in mind the following guidelines when making calls:</span></span>
  
- <span data-ttu-id="c4faf-117">Nunca confie ou use os valores de retorno de **IUnknown:: AddRef** ou **IUnknown:: Release**.</span><span class="sxs-lookup"><span data-stu-id="c4faf-117">Never rely on or use the return values from **IUnknown::AddRef** or **IUnknown::Release**.</span></span> <span data-ttu-id="c4faf-118">Esses valores de retorno são apenas para fins de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="c4faf-118">These return values are for diagnostic purposes only.</span></span> 
    
- <span data-ttu-id="c4faf-119">**IUnknown:: QueryInterface** sempre retorna erros com genéricos onde o recurso é FACILITY_NULL ou FACILITY_RPC, em vez de erros de MAPI.</span><span class="sxs-lookup"><span data-stu-id="c4faf-119">**IUnknown::QueryInterface** always returns generic COM errors where the facility is FACILITY_NULL or FACILITY_RPC, rather than MAPI errors.</span></span> 
    
- <span data-ttu-id="c4faf-120">Todos os outros métodos de interface retornam erros de interface MAPI com um recurso de erros do FACILITY_ITF ou do FACILITY_RPC ou do FACILITY_NULL.</span><span class="sxs-lookup"><span data-stu-id="c4faf-120">All other interface methods return MAPI interface errors with a facility of FACILITY_ITF, or FACILITY_RPC or FACILITY_NULL errors.</span></span>
    
<span data-ttu-id="c4faf-121">Quando uma chamada é feita para um método MAPI sem suporte, um dos quatro possíveis erros pode ser retornado:</span><span class="sxs-lookup"><span data-stu-id="c4faf-121">When a call is made to an unsupported MAPI method, one of four possible errors can be returned:</span></span> 
  
<span data-ttu-id="c4faf-122">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="c4faf-122">MAPI_E_NO_SUPPORT</span></span>
  
<span data-ttu-id="c4faf-123">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="c4faf-123">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span>
  
<span data-ttu-id="c4faf-124">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c4faf-124">MAPI_E_INVALID_PARAMETER</span></span>
  
<span data-ttu-id="c4faf-125">MAPI_E_VERSION.</span><span class="sxs-lookup"><span data-stu-id="c4faf-125">MAPI_E_VERSION.</span></span> 
  

