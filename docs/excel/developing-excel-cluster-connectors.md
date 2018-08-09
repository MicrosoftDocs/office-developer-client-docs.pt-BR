---
title: Desenvolvimento de conectores de cluster do Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b538ae44-37d2-496b-b6e7-b0e39f6e38cb
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 8c9a166ac06685c0a450e1e0bd60b2fbef67d336
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765255"
---
# <a name="developing-excel-cluster-connectors"></a><span data-ttu-id="4983e-103">Desenvolvimento de conectores de cluster do Excel</span><span class="sxs-lookup"><span data-stu-id="4983e-103">Developing Excel Cluster Connectors</span></span>

<span data-ttu-id="4983e-104">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4983e-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="4983e-105">Conectores de cluster do Excel fornecem um meio de descarregamento automaticamente chamadas de função definida pelo usuário do cluster-safe em um XLL para um servidor em cluster.</span><span class="sxs-lookup"><span data-stu-id="4983e-105">Excel cluster connectors provide a means for automatically offloading cluster-safe user-defined function calls in an XLL to a clustered server.</span></span> <span data-ttu-id="4983e-106">Para obter uma descrição das funções definidas pelo usuário de cluster-safe, consulte [Funções de segurança do Cluster](cluster-safe-functions.md).</span><span class="sxs-lookup"><span data-stu-id="4983e-106">For a description of cluster-safe user-defined functions, see [Cluster Safe Functions](cluster-safe-functions.md).</span></span> <span data-ttu-id="4983e-107">Esse descarregamento pode melhorar o desempenho, permitindo que os recursos de computação mais a ser usado.</span><span class="sxs-lookup"><span data-stu-id="4983e-107">This offloading can improve performance by enabling more computing resources to be used.</span></span> <span data-ttu-id="4983e-108">Um conector de cluster geralmente é desenvolvido por um fornecedor de cluster de computação de alto desempenho.</span><span class="sxs-lookup"><span data-stu-id="4983e-108">A cluster connector is typically developed by a high performance compute cluster vendor.</span></span>
  
## <a name="cluster-connectors"></a><span data-ttu-id="4983e-109">Conectores de cluster</span><span class="sxs-lookup"><span data-stu-id="4983e-109">Cluster Connectors</span></span>

<span data-ttu-id="4983e-110">Um conector de cluster é uma DLL que fornece os pontos de entrada definido que o Excel usa para coordenar as chamadas de função definida pelo usuário de cluster-safe.</span><span class="sxs-lookup"><span data-stu-id="4983e-110">A cluster connector is a DLL that provides defined entry points that Excel uses to coordinate cluster-safe user-defined function calls.</span></span> <span data-ttu-id="4983e-111">Ela serve como uma interface entre o Excel e o cluster de computação de alto desempenho, para sessão de gerenciamento, para tornar a função chama (passando o nome totalmente qualificado de função e argumentos de reais da chamada) e para retornar resultados de chamada para o Excel por meio de um mecanismo de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="4983e-111">It serves as an interface between Excel and the high-performance compute cluster, for session management, for making function calls (by passing the fully-qualified function name and the call's actual arguments), and for returning call results to Excel through a callback mechanism.</span></span>
  
<span data-ttu-id="4983e-112">Para criar um conector de cluster, crie uma DLL que expõe os pontos de entrada listados em [Funções de conector de Cluster do Excel](excel-cluster-connector-functions.md).</span><span class="sxs-lookup"><span data-stu-id="4983e-112">To create a cluster connector, create a DLL that exposes the entry points listed in [Excel Cluster Connector Functions](excel-cluster-connector-functions.md).</span></span>
  
## <a name="installing-a-cluster-connector"></a><span data-ttu-id="4983e-113">Instalando um conector de Cluster</span><span class="sxs-lookup"><span data-stu-id="4983e-113">Installing a Cluster Connector</span></span>

<span data-ttu-id="4983e-114">Para disponibilizar um conector de cluster no Excel, o código de programa de instalação do conector deve instalar a DLL do conector no computador onde o Excel está instalado.</span><span class="sxs-lookup"><span data-stu-id="4983e-114">To make a cluster connector available in Excel, the setup code of the connector must install the DLL of the connector on the computer where Excel is installed.</span></span> <span data-ttu-id="4983e-115">Além disso, o código de programa de instalação do conector deve adicionar uma entrada para o conector na seguinte chave do registro:</span><span class="sxs-lookup"><span data-stu-id="4983e-115">In addition, the setup code of the connector must add an entry for the connector under the following registry key:</span></span>
  
<span data-ttu-id="4983e-116">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel Connectors\ de Cluster</span><span class="sxs-lookup"><span data-stu-id="4983e-116">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel Cluster Connectors\\</span></span>
  
<span data-ttu-id="4983e-117">Adicione um nó a essa chave para o conector de cluster que especifica as cadeias de caracteres a seguintes:</span><span class="sxs-lookup"><span data-stu-id="4983e-117">Add a node to this key for the cluster connector that specifies the following strings:</span></span>
  
-  <span data-ttu-id="4983e-118">`Name`— o nome que aparecerá na lista de conectores de cluster no Excel.</span><span class="sxs-lookup"><span data-stu-id="4983e-118">`Name`—the name that will appear in the list of cluster connectors in Excel.</span></span>
    
-  <span data-ttu-id="4983e-119">`Filename`— o caminho completo para a DLL.</span><span class="sxs-lookup"><span data-stu-id="4983e-119">`Filename`—the full path for the DLL.</span></span>
    

