---
title: Desenvolver conectores de cluster do Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b538ae44-37d2-496b-b6e7-b0e39f6e38cb
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e1c70713586a7a143f119a2c3e9d34b982dcedba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412594"
---
# <a name="developing-excel-cluster-connectors"></a><span data-ttu-id="e72c4-103">Desenvolver conectores de cluster do Excel</span><span class="sxs-lookup"><span data-stu-id="e72c4-103">Developing Excel Cluster Connectors</span></span>

<span data-ttu-id="e72c4-104">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e72c4-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="e72c4-105">Os conectores de cluster do Excel fornecem meios para descarregar automaticamente as chamadas de função definidas pelo usuário com segurança de cluster em um servidor em cluster.</span><span class="sxs-lookup"><span data-stu-id="e72c4-105">Excel cluster connectors provide a means for automatically offloading cluster-safe user-defined function calls in an XLL to a clustered server.</span></span> <span data-ttu-id="e72c4-106">Para obter uma descrição das funções definidas pelo usuário com segurança de cluster, consulte [funções de segurança do cluster](cluster-safe-functions.md).</span><span class="sxs-lookup"><span data-stu-id="e72c4-106">For a description of cluster-safe user-defined functions, see [Cluster Safe Functions](cluster-safe-functions.md).</span></span> <span data-ttu-id="e72c4-107">Esse descarregamento pode melhorar o desempenho permitindo que mais recursos computacionais sejam usados.</span><span class="sxs-lookup"><span data-stu-id="e72c4-107">This offloading can improve performance by enabling more computing resources to be used.</span></span> <span data-ttu-id="e72c4-108">Um conector de cluster é normalmente desenvolvido por um fornecedor de cluster de computação de alto desempenho.</span><span class="sxs-lookup"><span data-stu-id="e72c4-108">A cluster connector is typically developed by a high performance compute cluster vendor.</span></span>
  
## <a name="cluster-connectors"></a><span data-ttu-id="e72c4-109">Conectores de cluster</span><span class="sxs-lookup"><span data-stu-id="e72c4-109">Cluster Connectors</span></span>

<span data-ttu-id="e72c4-110">Um conector de cluster é uma DLL que fornece pontos de entrada definidos que o Excel usa para coordenar chamadas de função definidas pelo usuário com segurança de cluster.</span><span class="sxs-lookup"><span data-stu-id="e72c4-110">A cluster connector is a DLL that provides defined entry points that Excel uses to coordinate cluster-safe user-defined function calls.</span></span> <span data-ttu-id="e72c4-111">Ele serve como uma interface entre o Excel e o cluster de computação de alto desempenho, para gerenciamento de sessão, para fazer chamadas de função (passando o nome de função totalmente qualificado e os argumentos reais da chamada) e para retornar os resultados da chamada para o Excel por meio de um mecanismo de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="e72c4-111">It serves as an interface between Excel and the high-performance compute cluster, for session management, for making function calls (by passing the fully-qualified function name and the call's actual arguments), and for returning call results to Excel through a callback mechanism.</span></span>
  
<span data-ttu-id="e72c4-112">Para criar um conector de cluster, crie uma DLL que expõe os pontos de entrada listados nas [funções do conector de cluster do Excel](excel-cluster-connector-functions.md).</span><span class="sxs-lookup"><span data-stu-id="e72c4-112">To create a cluster connector, create a DLL that exposes the entry points listed in [Excel Cluster Connector Functions](excel-cluster-connector-functions.md).</span></span>
  
## <a name="installing-a-cluster-connector"></a><span data-ttu-id="e72c4-113">Instalando um conector de cluster</span><span class="sxs-lookup"><span data-stu-id="e72c4-113">Installing a Cluster Connector</span></span>

<span data-ttu-id="e72c4-114">Para tornar um conector de cluster disponível no Excel, o código de instalação do conector deve instalar a DLL do conector no computador onde o Excel está instalado.</span><span class="sxs-lookup"><span data-stu-id="e72c4-114">To make a cluster connector available in Excel, the setup code of the connector must install the DLL of the connector on the computer where Excel is installed.</span></span> <span data-ttu-id="e72c4-115">Além disso, o código de configuração do conector deve adicionar uma entrada para o conector na seguinte chave do registro:</span><span class="sxs-lookup"><span data-stu-id="e72c4-115">In addition, the setup code of the connector must add an entry for the connector under the following registry key:</span></span>
  
<span data-ttu-id="e72c4-116">Conectores de cluster do HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel</span><span class="sxs-lookup"><span data-stu-id="e72c4-116">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel Cluster Connectors\\</span></span>
  
<span data-ttu-id="e72c4-117">Adicione um nó a essa chave para o conector de cluster que especifica as seguintes cadeias de caracteres:</span><span class="sxs-lookup"><span data-stu-id="e72c4-117">Add a node to this key for the cluster connector that specifies the following strings:</span></span>
  
-  <span data-ttu-id="e72c4-118">`Name`— o nome que aparecerá na lista de conectores de cluster no Excel.</span><span class="sxs-lookup"><span data-stu-id="e72c4-118">`Name`—the name that will appear in the list of cluster connectors in Excel.</span></span>
    
-  <span data-ttu-id="e72c4-119">`Filename`— o caminho completo da DLL.</span><span class="sxs-lookup"><span data-stu-id="e72c4-119">`Filename`—the full path for the DLL.</span></span>
    

