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
# <a name="error-handling-in-mapi"></a><span data-ttu-id="3b9a1-103">Tratamento de erros no MAPI</span><span class="sxs-lookup"><span data-stu-id="3b9a1-103">Error handling in MAPI</span></span>

<span data-ttu-id="3b9a1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3b9a1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3b9a1-105">Os valores de êxito, aviso e erro são retornados usando um número de 32 bits conhecido como alça de resultado ou HRESULT.</span><span class="sxs-lookup"><span data-stu-id="3b9a1-105">Success, warning, and error values are returned using a 32-bit number known as a result handle, or HRESULT.</span></span> <span data-ttu-id="3b9a1-106">Um HRESULT não é realmente um alça para nada; ele é simplesmente um valor de 32 bits com vários campos codificados no valor.</span><span class="sxs-lookup"><span data-stu-id="3b9a1-106">An HRESULT is really not a handle to anything; it is merely a 32-bit value with several fields encoded in the value.</span></span> <span data-ttu-id="3b9a1-107">Um resultado zero indica êxito e um resultado que não é zero indica falha.</span><span class="sxs-lookup"><span data-stu-id="3b9a1-107">A zero result indicates success and a nonzero result indicates failure.</span></span>
  
<span data-ttu-id="3b9a1-108">O MAPI em plataformas de 32 bits funciona exclusivamente com valores HRESULT.</span><span class="sxs-lookup"><span data-stu-id="3b9a1-108">MAPI on 32-bit platforms works solely with HRESULT values.</span></span>
  
<span data-ttu-id="3b9a1-109">A ilustração a seguir mostra o formato HRESULT para plataformas de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="3b9a1-109">The following illustration shows the HRESULT format for 32-bit platforms.</span></span>
  
<span data-ttu-id="3b9a1-110">**HRESULT format**</span><span class="sxs-lookup"><span data-stu-id="3b9a1-110">**HRESULT format**</span></span>
  
<span data-ttu-id="3b9a1-111">![Formato HRESULT](media/amapi_49.gif "formato HRESULT")</span><span class="sxs-lookup"><span data-stu-id="3b9a1-111">![HRESULT format](media/amapi_49.gif "HRESULT format")</span></span>
  
<span data-ttu-id="3b9a1-112">O bit de alta ordem no HRESULT indica se o valor de retorno representa sucesso ou falha.</span><span class="sxs-lookup"><span data-stu-id="3b9a1-112">The high order bit in the HRESULT indicates whether the return value represents success or failure.</span></span> <span data-ttu-id="3b9a1-113">Se for definido como zero, o valor indicará êxito.</span><span class="sxs-lookup"><span data-stu-id="3b9a1-113">If set to zero, the value indicates success.</span></span> <span data-ttu-id="3b9a1-114">Se definido como 1, indica falha.</span><span class="sxs-lookup"><span data-stu-id="3b9a1-114">If set to 1, it indicates failure.</span></span>
  
<span data-ttu-id="3b9a1-115">Os bits R, C, N e r são reservados no HRESULT.</span><span class="sxs-lookup"><span data-stu-id="3b9a1-115">The R, C, N, and r bits are reserved in the HRESULT.</span></span>
  
<span data-ttu-id="3b9a1-116">O campo de recurso em ambas as versões indica a área de responsabilidade do erro.</span><span class="sxs-lookup"><span data-stu-id="3b9a1-116">The facility field in both versions indicates the area of responsibility for the error.</span></span> <span data-ttu-id="3b9a1-117">Há várias instalações, mas a maioria dos erros de MAPI FACILITY_ITF para representar erros de interface.</span><span class="sxs-lookup"><span data-stu-id="3b9a1-117">There are several facilities, but the vast majority of MAPI errors use FACILITY_ITF to represent interface errors.</span></span> <span data-ttu-id="3b9a1-118">As instalações mais comuns usadas atualmente são: FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC e FACILITY_STORAGE.</span><span class="sxs-lookup"><span data-stu-id="3b9a1-118">The most common facilities that are currently used are: FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC, and FACILITY_STORAGE.</span></span> <span data-ttu-id="3b9a1-119">Se novas instalações são necessárias, a Microsoft as aloca porque elas precisam ser exclusivas.</span><span class="sxs-lookup"><span data-stu-id="3b9a1-119">If new facilities are necessary, Microsoft allocates them because they need to be unique.</span></span> <span data-ttu-id="3b9a1-120">A tabela a seguir descreve os vários campos de instalação.</span><span class="sxs-lookup"><span data-stu-id="3b9a1-120">The following table describes the various facility fields.</span></span>
  
|<span data-ttu-id="3b9a1-121">Facility</span><span class="sxs-lookup"><span data-stu-id="3b9a1-121">Facility</span></span>|<span data-ttu-id="3b9a1-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="3b9a1-122">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="3b9a1-123">FACILITY_NULL</span><span class="sxs-lookup"><span data-stu-id="3b9a1-123">FACILITY_NULL</span></span>  <br/> |<span data-ttu-id="3b9a1-124">Para códigos de status comuns amplamente aplicáveis, como S_OK ou E_OUTOF_MEMORY; o valor é zero.</span><span class="sxs-lookup"><span data-stu-id="3b9a1-124">For broadly applicable common status codes such as S_OK or E_OUTOF_MEMORY; the value is zero.</span></span>  <br/> |
|<span data-ttu-id="3b9a1-125">FACILITY_ITF</span><span class="sxs-lookup"><span data-stu-id="3b9a1-125">FACILITY_ITF</span></span>  <br/> |<span data-ttu-id="3b9a1-126">Para a maioria dos códigos de status retornados de métodos de interface; o valor é definido pela interface.</span><span class="sxs-lookup"><span data-stu-id="3b9a1-126">For most status codes returned from interface methods; the value is defined by the interface.</span></span> <span data-ttu-id="3b9a1-127">Ou seja, dois valores HRESULT com exatamente o mesmo valor de 32 bits retornado de duas interfaces diferentes podem ter significados diferentes.</span><span class="sxs-lookup"><span data-stu-id="3b9a1-127">That is, two HRESULT values with exactly the same 32-bit value returned from two different interfaces might have different meanings.</span></span>  <br/> |
|<span data-ttu-id="3b9a1-128">FACILITY_DISPATCH</span><span class="sxs-lookup"><span data-stu-id="3b9a1-128">FACILITY_DISPATCH</span></span>  <br/> |<span data-ttu-id="3b9a1-129">Para erros de interface [IDispatch](https://msdn.microsoft.com/library/ms221608.aspx) de associação tardia.</span><span class="sxs-lookup"><span data-stu-id="3b9a1-129">For late binding [IDispatch](https://msdn.microsoft.com/library/ms221608.aspx) interface errors.</span></span>  <br/> |
|<span data-ttu-id="3b9a1-130">FACILITY_RPC</span><span class="sxs-lookup"><span data-stu-id="3b9a1-130">FACILITY_RPC</span></span>  <br/> |<span data-ttu-id="3b9a1-131">Para códigos de status retornados de chamadas de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="3b9a1-131">For status codes returned from remote procedure calls.</span></span>  <br/> |
|<span data-ttu-id="3b9a1-132">FACILITY_STORAGE</span><span class="sxs-lookup"><span data-stu-id="3b9a1-132">FACILITY_STORAGE</span></span>  <br/> |<span data-ttu-id="3b9a1-133">Para códigos de status retornados de [chamadas de método IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) ou [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) relacionadas ao armazenamento estruturado.</span><span class="sxs-lookup"><span data-stu-id="3b9a1-133">For status codes returned from [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) or [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) method calls relating to structured storage.</span></span> <span data-ttu-id="3b9a1-134">Códigos de status com valores de código (16 bits inferiores) no intervalo de códigos de erro do Windows (ou seja, menos de 256) têm o mesmo significado que os erros do Windows correspondentes.</span><span class="sxs-lookup"><span data-stu-id="3b9a1-134">Status codes with code (lower 16 bits) values in the range of Windows error codes (that is, less than 256) have the same meaning as the corresponding Windows errors.</span></span>  <br/> |
   
<span data-ttu-id="3b9a1-135">O campo de código é um número exclusivo atribuído para representar o erro ou aviso.</span><span class="sxs-lookup"><span data-stu-id="3b9a1-135">The code field is a unique number that is assigned to represent the error or warning.</span></span>
  

