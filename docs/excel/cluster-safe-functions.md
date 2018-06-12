---
title: Funções de segurança de cluster
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 787badaf-8782-454d-a016-7eae83bbd8a9
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: f73f49e4d76a8545399eede283b70551ee6569f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765252"
---
# <a name="cluster-safe-functions"></a><span data-ttu-id="59eb6-103">Funções de segurança de cluster</span><span class="sxs-lookup"><span data-stu-id="59eb6-103">Cluster safe functions</span></span>

<span data-ttu-id="59eb6-104">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="59eb6-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="59eb6-105">No Excel 2013, Excel pode descarregamento de chamadas de função definida pelo usuário (UDF) para um cluster de computação de alto desempenho por meio de uma interface de conector de cluster dedicado.</span><span class="sxs-lookup"><span data-stu-id="59eb6-105">In Excel 2013, Excel can offload User-Defined Function (UDF) calls to a high-performance computing cluster through a dedicated cluster connector interface.</span></span> <span data-ttu-id="59eb6-106">Compute cluster fornecedores fornecem conectores de Cluster.</span><span class="sxs-lookup"><span data-stu-id="59eb6-106">Compute cluster vendors provide Cluster Connectors.</span></span> <span data-ttu-id="59eb6-107">Os autores do UDF podem declarar seus UDFs como cluster seguros e, quando um conector de cluster estiver presente, o Excel envia chamadas para esses UDFs para o conector de cluster para descarregamento.</span><span class="sxs-lookup"><span data-stu-id="59eb6-107">UDF authors can declare their UDFs as cluster safe and then, when a cluster connector is present, Excel sends calls to these UDFs to the cluster connector for offloading.</span></span>
  
<span data-ttu-id="59eb6-108">Quando o Excel descobre um UDF seguras do cluster durante o recálculo, ele passa o nome da XLL que está sendo executado, o nome do UDF seguras do cluster e qualquer parâmetro para o conector de cluster.</span><span class="sxs-lookup"><span data-stu-id="59eb6-108">When Excel discovers a cluster-safe UDF during recalculation, it passes the name of the XLL that is currently running, the name of the cluster-safe UDF, and any parameters to the cluster connector.</span></span> <span data-ttu-id="59eb6-109">O conector é executado a chamada UDF remotamente e retorna os resultados para o Excel.</span><span class="sxs-lookup"><span data-stu-id="59eb6-109">The connector runs the UDF call remotely and returns the results to Excel.</span></span> <span data-ttu-id="59eb6-110">Cálculo dependentes não continuará e quando o conector de cluster concluiu a execução do UDF, ele passa os resultados para o Excel e continuam cálculos dependentes.</span><span class="sxs-lookup"><span data-stu-id="59eb6-110">Non-dependent calculation continues and when the cluster connector has finished running the UDF, it passes the results to Excel and dependent calculations continue.</span></span> <span data-ttu-id="59eb6-111">O mecanismo para esse comportamento assíncrono simule o mecanismo usado pela UDFs assíncronas, exceto pelo fato do conector de cluster gerencia os aspectos assíncronos, em vez de autor UDF.</span><span class="sxs-lookup"><span data-stu-id="59eb6-111">The mechanism for this asynchronous behavior mimics the mechanism used by asynchronous UDFs, except that the cluster connector manages the asynchronous aspects instead of the UDF author.</span></span> <span data-ttu-id="59eb6-112">Normalmente, um conector de cluster implementa uma correção XLL para carregar XLLs e execute UDFs em compute nós do cluster.</span><span class="sxs-lookup"><span data-stu-id="59eb6-112">Typically, a cluster connector implements an XLL shim to load XLLs and run UDFs on compute cluster nodes.</span></span>
  
<span data-ttu-id="59eb6-113">A mecânica da declarando UDFs como cluster-safe são semelhantes às declarando UDFs como seguros para recálculo multithread.</span><span class="sxs-lookup"><span data-stu-id="59eb6-113">The mechanics of declaring UDFs as cluster-safe resemble those of declaring UDFs as safe for multi-threaded recalculation.</span></span> <span data-ttu-id="59eb6-114">No entanto, porque o UDF não necessariamente estiver em execução no mesmo computador que outros UDFs da mesma sessão do Excel, existem diferentes considerações ao escrever UDFs seguras do cluster.</span><span class="sxs-lookup"><span data-stu-id="59eb6-114">However, because the UDF is not necessarily running on the same computer as other UDFs from the same Excel session, there are different considerations when writing cluster-safe UDFs.</span></span>
  
<span data-ttu-id="59eb6-115">Para registrar um UDF como seguras do cluster, você deve chamar a função de retorno de chamada [xlfRegister (formulário 1)](xlfregister-form-1.md) por meio da interface **Excel12** ou **Excel12v** .</span><span class="sxs-lookup"><span data-stu-id="59eb6-115">To register a UDF as cluster-safe, you must call the [xlfRegister (Form 1)](xlfregister-form-1.md) callback function through the **Excel12** or **Excel12v** interface.</span></span> <span data-ttu-id="59eb6-116">Para obter mais informações sobre essas interfaces, consulte o [Excel4/Excel12](excel4-excel12.md) e [Excel4v/Excel12v](excel4v-excel12v.md).</span><span class="sxs-lookup"><span data-stu-id="59eb6-116">For more information about these interfaces, see the [Excel4/Excel12](excel4-excel12.md) and [Excel4v/Excel12v](excel4v-excel12v.md).</span></span> <span data-ttu-id="59eb6-117">Registrando um UDF como não há suporte para cluster-safe por meio da interface do **Excel4** ou **Excel4v** .</span><span class="sxs-lookup"><span data-stu-id="59eb6-117">Registering a UDF as cluster-safe through the **Excel4** or **Excel4v** interface is not supported.</span></span> 
  
<span data-ttu-id="59eb6-118">Se você registrar uma função como cluster-safe, certifique-se de que a função se comporta de forma segura de cluster.</span><span class="sxs-lookup"><span data-stu-id="59eb6-118">If you register a function as cluster-safe, you must ensure that the function behaves in a cluster-safe way.</span></span> <span data-ttu-id="59eb6-119">Embora o comportamento exato do conector do cluster é específico da implementação, você deve projetar sua UDF sejam executados em um sistema de computador distribuído e que têm as seguintes características:</span><span class="sxs-lookup"><span data-stu-id="59eb6-119">Although the exact behavior of the cluster connector is implementation-specific, you should design your UDF to run on a distributed computer system and to have the following characteristics:</span></span>
  
- <span data-ttu-id="59eb6-120">Um UDF não deve confiar em qualquer estado de memória.</span><span class="sxs-lookup"><span data-stu-id="59eb6-120">A UDF should not rely on any memory state.</span></span> <span data-ttu-id="59eb6-121">Por exemplo, um UDF não deve confiar em um cache de memória existente.</span><span class="sxs-lookup"><span data-stu-id="59eb6-121">For example, a UDF should not rely on an existing in-memory cache.</span></span>
    
- <span data-ttu-id="59eb6-122">Um UDF não deve realizar retornos de chamada do Excel que não suporta o provedor do conector de cluster.</span><span class="sxs-lookup"><span data-stu-id="59eb6-122">A UDF should not perform Excel callbacks that the cluster connector provider does not support.</span></span>
    
<span data-ttu-id="59eb6-123">Além de comportamento de cluster-safe, existem as seguintes restrições técnicas sobre UDFs seguras do cluster:</span><span class="sxs-lookup"><span data-stu-id="59eb6-123">In addition to cluster-safe behavior, there are the following technical restrictions on cluster-safe UDFs:</span></span>
  
1. <span data-ttu-id="59eb6-124">Sem argumentos XLOPER (tipos 'P', 'R').</span><span class="sxs-lookup"><span data-stu-id="59eb6-124">No XLOPER arguments (types 'P', 'R').</span></span>
    
2. <span data-ttu-id="59eb6-125">Sem argumentos XLOPER12 que oferecem suporte a referências de intervalo (tipo 'U').</span><span class="sxs-lookup"><span data-stu-id="59eb6-125">No XLOPER12 arguments that support range references (type 'U').</span></span>
    
3. <span data-ttu-id="59eb6-126">Não pode ser uma função equivalente de folha de macro ('#' e '&amp;' não pode ser combinado).</span><span class="sxs-lookup"><span data-stu-id="59eb6-126">Cannot be a macro sheet equivalent function ('#' and '&amp;' cannot be combined).</span></span>
    
<span data-ttu-id="59eb6-127">Para UDFs com mais curto tempo de execução, a sobrecarga de descarregamento pode ser maior do que o tempo que leva UDF ser executados, eliminando muitos dos benefícios do uso dessa infra-estrutura.</span><span class="sxs-lookup"><span data-stu-id="59eb6-127">For UDFs with shorter execution times, the overhead of offloading may be larger than the time it takes the UDF to execute, negating many of the benefits of using this infrastructure.</span></span>
  
> [!NOTE]
> <span data-ttu-id="59eb6-128">Você não pode declarar um UDF seguras do cluster como uma UDF assíncrona.</span><span class="sxs-lookup"><span data-stu-id="59eb6-128">You cannot declare a cluster-safe UDF as an asynchronous UDF.</span></span> 
  
<span data-ttu-id="59eb6-129">Um UDF para determinar se ele está sendo executado usando um conector de cluster chamando a função de retorno de chamada [xlRunningOnCluster](xlrunningoncluster.md) .</span><span class="sxs-lookup"><span data-stu-id="59eb6-129">A UDF can determine whether it is being run using a cluster connector by calling the [xlRunningOnCluster](xlrunningoncluster.md) callback function.</span></span> 
  

