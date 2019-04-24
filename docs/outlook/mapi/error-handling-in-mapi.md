---
title: Tratamento de erros no MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99e2c485-af84-46f4-84b4-fca2117b5a21
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 98ee0856411cce3a3e9012185be6c30503de7779
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287274"
---
# <a name="error-handling-in-mapi"></a><span data-ttu-id="44485-103">Tratamento de erros no MAPI</span><span class="sxs-lookup"><span data-stu-id="44485-103">Error handling in MAPI</span></span>

<span data-ttu-id="44485-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44485-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44485-105">Os valores Success, Warning e Error são retornados usando um número de 32 bits conhecido como um identificador de resultado ou HRESULT.</span><span class="sxs-lookup"><span data-stu-id="44485-105">Success, warning, and error values are returned using a 32-bit number known as a result handle, or HRESULT.</span></span> <span data-ttu-id="44485-106">No entanto, o HRESULT não é um manipulador para nada; é meramente um valor de 32 bits com vários campos codificados no valor.</span><span class="sxs-lookup"><span data-stu-id="44485-106">An HRESULT is really not a handle to anything; it is merely a 32-bit value with several fields encoded in the value.</span></span> <span data-ttu-id="44485-107">Um resultado zero indica êxito e um resultado diferente de zero indica falha.</span><span class="sxs-lookup"><span data-stu-id="44485-107">A zero result indicates success and a nonzero result indicates failure.</span></span>
  
<span data-ttu-id="44485-108">MAPI em plataformas de 32 bits funciona unicamente com valores HRESULT.</span><span class="sxs-lookup"><span data-stu-id="44485-108">MAPI on 32-bit platforms works solely with HRESULT values.</span></span>
  
<span data-ttu-id="44485-109">A ilustração a seguir mostra o formato HRESULT para plataformas de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="44485-109">The following illustration shows the HRESULT format for 32-bit platforms.</span></span>
  
<span data-ttu-id="44485-110">**HRESULT format**</span><span class="sxs-lookup"><span data-stu-id="44485-110">**HRESULT format**</span></span>
  
<span data-ttu-id="44485-111">![Formato HRESULT] (media/amapi_49.gif "Formato HRESULT")</span><span class="sxs-lookup"><span data-stu-id="44485-111">![HRESULT format](media/amapi_49.gif "HRESULT format")</span></span>
  
<span data-ttu-id="44485-112">O bit de ordem superior no HRESULT indica se o valor de retorno representa êxito ou falha.</span><span class="sxs-lookup"><span data-stu-id="44485-112">The high order bit in the HRESULT indicates whether the return value represents success or failure.</span></span> <span data-ttu-id="44485-113">Se definido como zero, o valor indica êxito.</span><span class="sxs-lookup"><span data-stu-id="44485-113">If set to zero, the value indicates success.</span></span> <span data-ttu-id="44485-114">Se definido como 1, indica falha.</span><span class="sxs-lookup"><span data-stu-id="44485-114">If set to 1, it indicates failure.</span></span>
  
<span data-ttu-id="44485-115">Os bits R, C, N e R são reservados no HRESULT.</span><span class="sxs-lookup"><span data-stu-id="44485-115">The R, C, N, and r bits are reserved in the HRESULT.</span></span>
  
<span data-ttu-id="44485-116">O campo recurso em ambas as versões indica a área de responsabilidade do erro.</span><span class="sxs-lookup"><span data-stu-id="44485-116">The facility field in both versions indicates the area of responsibility for the error.</span></span> <span data-ttu-id="44485-117">Há vários recursos, mas a maior parte dos erros MAPI usa o FACILITY_ITF para representar erros de interface.</span><span class="sxs-lookup"><span data-stu-id="44485-117">There are several facilities, but the vast majority of MAPI errors use FACILITY_ITF to represent interface errors.</span></span> <span data-ttu-id="44485-118">Os recursos mais comuns usados atualmente são: FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC e FACILITY_STORAGE.</span><span class="sxs-lookup"><span data-stu-id="44485-118">The most common facilities that are currently used are: FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC, and FACILITY_STORAGE.</span></span> <span data-ttu-id="44485-119">Se novos recursos forem necessários, a Microsoft os alocará porque eles precisam ser exclusivos.</span><span class="sxs-lookup"><span data-stu-id="44485-119">If new facilities are necessary, Microsoft allocates them because they need to be unique.</span></span> <span data-ttu-id="44485-120">A tabela a seguir descreve os vários campos de recurso.</span><span class="sxs-lookup"><span data-stu-id="44485-120">The following table describes the various facility fields.</span></span>
  
|<span data-ttu-id="44485-121">Facility</span><span class="sxs-lookup"><span data-stu-id="44485-121">Facility</span></span>|<span data-ttu-id="44485-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="44485-122">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="44485-123">FACILITY_NULL</span><span class="sxs-lookup"><span data-stu-id="44485-123">FACILITY_NULL</span></span>  <br/> |<span data-ttu-id="44485-124">Para códigos de status comuns amplamente aplicáveis, como S_OK ou E_OUTOF_MEMORY; o valor é zero.</span><span class="sxs-lookup"><span data-stu-id="44485-124">For broadly applicable common status codes such as S_OK or E_OUTOF_MEMORY; the value is zero.</span></span>  <br/> |
|<span data-ttu-id="44485-125">FACILITY_ITF</span><span class="sxs-lookup"><span data-stu-id="44485-125">FACILITY_ITF</span></span>  <br/> |<span data-ttu-id="44485-126">Para a maioria dos códigos de status retornados dos métodos de interface; o valor é definido pela interface.</span><span class="sxs-lookup"><span data-stu-id="44485-126">For most status codes returned from interface methods; the value is defined by the interface.</span></span> <span data-ttu-id="44485-127">Ou seja, dois valores HRESULT com exatamente o mesmo valor de 32 bits retornado de duas interfaces diferentes podem ter significados diferentes.</span><span class="sxs-lookup"><span data-stu-id="44485-127">That is, two HRESULT values with exactly the same 32-bit value returned from two different interfaces might have different meanings.</span></span>  <br/> |
|<span data-ttu-id="44485-128">FACILITY_DISPATCH</span><span class="sxs-lookup"><span data-stu-id="44485-128">FACILITY_DISPATCH</span></span>  <br/> |<span data-ttu-id="44485-129">Para erros de [](https://msdn.microsoft.com/library/ms221608.aspx) interface de associação tardia.</span><span class="sxs-lookup"><span data-stu-id="44485-129">For late binding [IDispatch](https://msdn.microsoft.com/library/ms221608.aspx) interface errors.</span></span>  <br/> |
|<span data-ttu-id="44485-130">FACILITY_RPC</span><span class="sxs-lookup"><span data-stu-id="44485-130">FACILITY_RPC</span></span>  <br/> |<span data-ttu-id="44485-131">Para códigos de status retornados de chamadas de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="44485-131">For status codes returned from remote procedure calls.</span></span>  <br/> |
|<span data-ttu-id="44485-132">FACILITY_STORAGE</span><span class="sxs-lookup"><span data-stu-id="44485-132">FACILITY_STORAGE</span></span>  <br/> |<span data-ttu-id="44485-133">Para códigos de status retornados das chamadas de método [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) ou [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) relacionadas ao armazenamento estruturado.</span><span class="sxs-lookup"><span data-stu-id="44485-133">For status codes returned from [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) or [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) method calls relating to structured storage.</span></span> <span data-ttu-id="44485-134">Os códigos de status com valores de código (menores de 16 bits) no intervalo de códigos de erro do Windows (ou seja, menos de 256) têm o mesmo significado dos erros do Windows correspondentes.</span><span class="sxs-lookup"><span data-stu-id="44485-134">Status codes with code (lower 16 bits) values in the range of Windows error codes (that is, less than 256) have the same meaning as the corresponding Windows errors.</span></span>  <br/> |
   
<span data-ttu-id="44485-135">O campo de código é um número exclusivo que é atribuído para representar o erro ou aviso.</span><span class="sxs-lookup"><span data-stu-id="44485-135">The code field is a unique number that is assigned to represent the error or warning.</span></span>
  

