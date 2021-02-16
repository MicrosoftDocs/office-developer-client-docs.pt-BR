---
title: Funções seguras de cluster
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 787badaf-8782-454d-a016-7eae83bbd8a9
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d32925fcd5c3be7fe3e615ee2290f25c7595911c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409297"
---
# <a name="cluster-safe-functions"></a><span data-ttu-id="4cd77-103">Funções seguras de cluster</span><span class="sxs-lookup"><span data-stu-id="4cd77-103">Cluster safe functions</span></span>

<span data-ttu-id="4cd77-104">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4cd77-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="4cd77-105">No Excel 2013, o Excel pode descarregar chamadas User-Defined Function (UDF) para um cluster de computação de alto desempenho por meio de uma interface de conector de cluster dedicada.</span><span class="sxs-lookup"><span data-stu-id="4cd77-105">In Excel 2013, Excel can offload User-Defined Function (UDF) calls to a high-performance computing cluster through a dedicated cluster connector interface.</span></span> <span data-ttu-id="4cd77-106">Os fornecedores de cluster de computação fornecem Conectores de Cluster.</span><span class="sxs-lookup"><span data-stu-id="4cd77-106">Compute cluster vendors provide Cluster Connectors.</span></span> <span data-ttu-id="4cd77-107">Os autores UDF podem declarar suas UDFs como seguras de cluster e, quando um conector de cluster estiver presente, o Excel envia chamadas para essas UDFs para o conector de cluster para descarregamento.</span><span class="sxs-lookup"><span data-stu-id="4cd77-107">UDF authors can declare their UDFs as cluster safe and then, when a cluster connector is present, Excel sends calls to these UDFs to the cluster connector for offloading.</span></span>
  
<span data-ttu-id="4cd77-108">Quando o Excel descobre uma UDF segura para cluster durante o recálculo, ele passa o nome do XLL em execução no momento, o nome da UDF segura para cluster e quaisquer parâmetros para o conector do cluster.</span><span class="sxs-lookup"><span data-stu-id="4cd77-108">When Excel discovers a cluster-safe UDF during recalculation, it passes the name of the XLL that is currently running, the name of the cluster-safe UDF, and any parameters to the cluster connector.</span></span> <span data-ttu-id="4cd77-109">O conector executa a chamada UDF remotamente e retorna os resultados para o Excel.</span><span class="sxs-lookup"><span data-stu-id="4cd77-109">The connector runs the UDF call remotely and returns the results to Excel.</span></span> <span data-ttu-id="4cd77-110">O cálculo não dependente continua e, quando o conector de cluster termina de executar o UDF, ele passa os resultados para o Excel e os cálculos dependentes continuam.</span><span class="sxs-lookup"><span data-stu-id="4cd77-110">Non-dependent calculation continues and when the cluster connector has finished running the UDF, it passes the results to Excel and dependent calculations continue.</span></span> <span data-ttu-id="4cd77-111">O mecanismo para esse comportamento assíncrono imita o mecanismo usado por UDFs assíncronas, exceto que o conector de cluster gerencia os aspectos assíncronos em vez do autor UDF.</span><span class="sxs-lookup"><span data-stu-id="4cd77-111">The mechanism for this asynchronous behavior mimics the mechanism used by asynchronous UDFs, except that the cluster connector manages the asynchronous aspects instead of the UDF author.</span></span> <span data-ttu-id="4cd77-112">Normalmente, um conector de cluster implementa um shim XLL para carregar XLLs e executar UDFs em nós de cluster de computação.</span><span class="sxs-lookup"><span data-stu-id="4cd77-112">Typically, a cluster connector implements an XLL shim to load XLLs and run UDFs on compute cluster nodes.</span></span>
  
<span data-ttu-id="4cd77-113">A mecânica de declaração de UDFs como seguras para cluster é semelhante às de declarar UDFs como seguras para recálculo multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="4cd77-113">The mechanics of declaring UDFs as cluster-safe resemble those of declaring UDFs as safe for multi-threaded recalculation.</span></span> <span data-ttu-id="4cd77-114">No entanto, como o UDF não está necessariamente sendo executado no mesmo computador que outras UDFs da mesma sessão do Excel, há considerações diferentes ao escrever UDFs seguras para cluster.</span><span class="sxs-lookup"><span data-stu-id="4cd77-114">However, because the UDF is not necessarily running on the same computer as other UDFs from the same Excel session, there are different considerations when writing cluster-safe UDFs.</span></span>
  
<span data-ttu-id="4cd77-115">Para registrar uma UDF como segura para cluster, você deve chamar a função de retorno de chamada [xlfRegister (Formulário 1)](xlfregister-form-1.md) por meio da interface **Excel12** ou **Excel12v.**</span><span class="sxs-lookup"><span data-stu-id="4cd77-115">To register a UDF as cluster-safe, you must call the [xlfRegister (Form 1)](xlfregister-form-1.md) callback function through the **Excel12** or **Excel12v** interface.</span></span> <span data-ttu-id="4cd77-116">Para obter mais informações sobre essas interfaces, consulte [Excel4/Excel12](excel4-excel12.md) e [Excel4v/Excel12v](excel4v-excel12v.md).</span><span class="sxs-lookup"><span data-stu-id="4cd77-116">For more information about these interfaces, see the [Excel4/Excel12](excel4-excel12.md) and [Excel4v/Excel12v](excel4v-excel12v.md).</span></span> <span data-ttu-id="4cd77-117">Não há suporte para o registro de uma UDF como segura para cluster por meio da interface **Excel4** ou **Excel4v.**</span><span class="sxs-lookup"><span data-stu-id="4cd77-117">Registering a UDF as cluster-safe through the **Excel4** or **Excel4v** interface is not supported.</span></span> 
  
<span data-ttu-id="4cd77-118">Se você registrar uma função como segura para cluster, deverá garantir que a função se comporte de maneira segura para cluster.</span><span class="sxs-lookup"><span data-stu-id="4cd77-118">If you register a function as cluster-safe, you must ensure that the function behaves in a cluster-safe way.</span></span> <span data-ttu-id="4cd77-119">Embora o comportamento exato do conector de cluster seja específico da implementação, você deve projetar o UDF para ser executado em um sistema de computador distribuído e ter as seguintes características:</span><span class="sxs-lookup"><span data-stu-id="4cd77-119">Although the exact behavior of the cluster connector is implementation-specific, you should design your UDF to run on a distributed computer system and to have the following characteristics:</span></span>
  
- <span data-ttu-id="4cd77-120">Uma UDF não deve depender de nenhum estado de memória.</span><span class="sxs-lookup"><span data-stu-id="4cd77-120">A UDF should not rely on any memory state.</span></span> <span data-ttu-id="4cd77-121">Por exemplo, uma UDF não deve depender de um cache existente na memória.</span><span class="sxs-lookup"><span data-stu-id="4cd77-121">For example, a UDF should not rely on an existing in-memory cache.</span></span>
    
- <span data-ttu-id="4cd77-122">A UDF should not perform Excel callbacks that the cluster connector provider does not support.</span><span class="sxs-lookup"><span data-stu-id="4cd77-122">A UDF should not perform Excel callbacks that the cluster connector provider does not support.</span></span>
    
<span data-ttu-id="4cd77-123">Além do comportamento seguro para cluster, há as seguintes restrições técnicas em UDFs seguras para cluster:</span><span class="sxs-lookup"><span data-stu-id="4cd77-123">In addition to cluster-safe behavior, there are the following technical restrictions on cluster-safe UDFs:</span></span>
  
1. <span data-ttu-id="4cd77-124">Nenhum argumento XLOPER (tipos 'P', 'R').</span><span class="sxs-lookup"><span data-stu-id="4cd77-124">No XLOPER arguments (types 'P', 'R').</span></span>
    
2. <span data-ttu-id="4cd77-125">Nenhum argumento XLOPER12 que suporte referências de intervalo (tipo 'U').</span><span class="sxs-lookup"><span data-stu-id="4cd77-125">No XLOPER12 arguments that support range references (type 'U').</span></span>
    
3. <span data-ttu-id="4cd77-126">Não pode ser uma função equivalente de planilha de macro ('#' e &amp; ' ' não podem ser combinadas).</span><span class="sxs-lookup"><span data-stu-id="4cd77-126">Cannot be a macro sheet equivalent function ('#' and '&amp;' cannot be combined).</span></span>
    
<span data-ttu-id="4cd77-127">Para UDFs com tempos de execução mais curtos, a sobrecarga de descarregamento pode ser maior do que o tempo que leva para a UDF ser executada, anulando muitos dos benefícios de usar essa infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="4cd77-127">For UDFs with shorter execution times, the overhead of offloading may be larger than the time it takes the UDF to execute, negating many of the benefits of using this infrastructure.</span></span>
  
> [!NOTE]
> <span data-ttu-id="4cd77-128">Você não pode declarar uma UDF segura para cluster como uma UDF assíncrona.</span><span class="sxs-lookup"><span data-stu-id="4cd77-128">You cannot declare a cluster-safe UDF as an asynchronous UDF.</span></span> 
  
<span data-ttu-id="4cd77-129">Uma UDF pode determinar se está sendo executado usando um conector de cluster chamando a função de retorno de chamada [xlRunningOnCluster.](xlrunningoncluster.md)</span><span class="sxs-lookup"><span data-stu-id="4cd77-129">A UDF can determine whether it is being run using a cluster connector by calling the [xlRunningOnCluster](xlrunningoncluster.md) callback function.</span></span> 
  

