---
title: Soluções para o acesso remoto a dados
TOCTitle: Solutions for Remote Data Access
ms:assetid: ae84c05a-cf9b-2b4c-4d7a-e6c9dcd120c1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249825(v=office.15)
ms:contentKeyID: 48547072
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b64ed19c268874e0e52a87bc2e05aacb6083422
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306899"
---
# <a name="solutions-for-remote-data-access"></a><span data-ttu-id="f8ab2-102">Soluções para o acesso a dados remotos</span><span class="sxs-lookup"><span data-stu-id="f8ab2-102">Solutions for Remote Data Access</span></span>

<span data-ttu-id="f8ab2-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f8ab2-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="the-issue"></a><span data-ttu-id="f8ab2-104">O problema</span><span class="sxs-lookup"><span data-stu-id="f8ab2-104">The issue</span></span>

<span data-ttu-id="f8ab2-p101">O ADO permite que seu aplicativo obtenha acesso direto às fontes de dados (algumas vezes, chamado de sistema de duas camadas) e modifique-as. Por exemplo, se sua conexão for estabelecida com a fonte de dados que contém seus dados, ela será uma conexão direta em um sistema de duas camadas.</span><span class="sxs-lookup"><span data-stu-id="f8ab2-p101">ADO enables your application to directly gain access to and modify data sources (sometimes called a two-tier system). For example, if your connection is to the data source that contains your data, that is a direct connection in a two-tier system.</span></span>

<span data-ttu-id="f8ab2-107">No enTanto, você pode querer acessar fontes de dados indiretamente por meio de um intermediário, como o Microsoft Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="f8ab2-107">However, you may want to access data sources indirectly through an intermediary such as Microsoft Internet Information Services (IIS).</span></span> <span data-ttu-id="f8ab2-108">Essa organização algumas vezes é chamada de sistema de três camadas.</span><span class="sxs-lookup"><span data-stu-id="f8ab2-108">This arrangement is sometimes called a three-tier system.</span></span> <span data-ttu-id="f8ab2-109">O IIS é um sistema cliente/servidor que oferece uma forma eficiente de um aplicativo local, ou cliente, chamar um programa remoto, ou de servidor, pela Internet ou por uma intranet.</span><span class="sxs-lookup"><span data-stu-id="f8ab2-109">IIS is a client/server system that provides an efficient way for a local, or client, application to invoke a remote, or server, program across the Internet or an intranet.</span></span> <span data-ttu-id="f8ab2-110">O programa de servidor obtém acesso à fonte de dados e, opcionalmente, processa os dados adquiridos.</span><span class="sxs-lookup"><span data-stu-id="f8ab2-110">The server program gains access to the data source and optionally processes the acquired data.</span></span>

<span data-ttu-id="f8ab2-111">Por exemplo, sua página da Web na intranet contém um aplicativo escrito no Microsoft Visual Basic Scripting Edition (VBScript), que se conecta ao IIS.</span><span class="sxs-lookup"><span data-stu-id="f8ab2-111">For example, your intranet webpage contains an application written in Microsoft Visual Basic Scripting Edition (VBScript), which connects to IIS.</span></span> <span data-ttu-id="f8ab2-112">O IIS, por sua vez, conecta-se à fonte de dados real, recupera os dados, processa-os de alguma maneira e retorna as informações processadas ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f8ab2-112">IIS in turn connects to the actual data source, retrieves the data, processes it in some way, and then returns the processed information to your application.</span></span>

<span data-ttu-id="f8ab2-113">Neste exemplo, seu aplicativo nunca esteve diretamente conectado à fonte de dados, ao contrário do IIS.</span><span class="sxs-lookup"><span data-stu-id="f8ab2-113">In this example, your application never directly connected to the data source; IIS did.</span></span> <span data-ttu-id="f8ab2-114">Além disso, o IIS acessou os dados através do ADO.</span><span class="sxs-lookup"><span data-stu-id="f8ab2-114">And IIS accessed the data by means of ADO.</span></span>

> [!NOTE]
> <span data-ttu-id="f8ab2-115">O aplicativo cliente/servidor não precisa ser baseado na Internet ou em uma intranet (ou seja, baseado na Web) — ele pode consistir exclusivamente de programas compilados em uma rede local.</span><span class="sxs-lookup"><span data-stu-id="f8ab2-115">The client/server application does not have to be based on the Internet or an intranet (that is, web-based)—it could consist solely of compiled programs on a local area network.</span></span> <span data-ttu-id="f8ab2-116">No enTanto, o caso típico é um aplicativo baseado na Web.</span><span class="sxs-lookup"><span data-stu-id="f8ab2-116">However, the typical case is a web-based application.</span></span>

<span data-ttu-id="f8ab2-117">Como alguns controles visuais, como grade, caixa de seleção ou lista, podem usar as informações retornadas, essas informações devem ser facilmente usadas por esses controles.</span><span class="sxs-lookup"><span data-stu-id="f8ab2-117">Because some visual control, such as a grid, check box, or list, may use the returned information, the returned information must be easily used by a visual control.</span></span>

<span data-ttu-id="f8ab2-p106">Você deseja uma interface de programação de aplicativo simples e eficiente que ofereça suporte a sistemas de três camadas e retorne informações com a mesma facilidade que ocorre com a recuperação em um sistema de duas camadas. O RDS (Remote Data Service) é essa interface.</span><span class="sxs-lookup"><span data-stu-id="f8ab2-p106">You want a simple and efficient application-programming interface that supports three-tier systems, and returns information as easily as if it had been retrieved on a two-tier system. Remote Data Service (RDS) is this interface.</span></span>

## <a name="the-solution"></a><span data-ttu-id="f8ab2-120">A solução</span><span class="sxs-lookup"><span data-stu-id="f8ab2-120">The solution</span></span>

<span data-ttu-id="f8ab2-121">O RDS define um modelo de programação – a sequência de atividades necessárias para acessar e atualizar uma fonte de dados, para obter acesso aos dados por meio de um intermediário, como o serviços de informações da Internet (IIS).</span><span class="sxs-lookup"><span data-stu-id="f8ab2-121">RDS defines a programming model—the sequence of activities necessary to gain access to and update a data source — to gain access to data through an intermediary, such as Internet Information Services (IIS).</span></span> <span data-ttu-id="f8ab2-122">O modelo de programação resume toda a funcionalidade do RDS.</span><span class="sxs-lookup"><span data-stu-id="f8ab2-122">The programming model summarizes the entire functionality of RDS.</span></span>

