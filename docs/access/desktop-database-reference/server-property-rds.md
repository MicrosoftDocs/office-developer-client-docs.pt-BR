---
title: Propriedade Server (RDS)
TOCTitle: Server Property (RDS)
ms:assetid: 17519dbe-a43a-1d0d-22c1-dc0def2f63ab
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248926(v=office.15)
ms:contentKeyID: 48543448
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 487b6e676816ab571cb08f6cfe7870362c7a8c84
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868431"
---
# <a name="server-property-rds"></a><span data-ttu-id="ab309-102">Propriedade Server (RDS)</span><span class="sxs-lookup"><span data-stu-id="ab309-102">Server Property (RDS)</span></span>


<span data-ttu-id="ab309-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="ab309-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ab309-104">Indica o nome do IIS (Serviços de Informações da Internet) e o protocolo de comunicação.</span><span class="sxs-lookup"><span data-stu-id="ab309-104">Indicates the Internet Information Services (IIS) name and communication protocol.</span></span>

<span data-ttu-id="ab309-105">Você pode definir a propriedade **Server** no tempo de design nas marcas OBJECT do objeto [RDS.DataControl](datacontrol-object-rds.md) ou em tempo de execução no código de script.</span><span class="sxs-lookup"><span data-stu-id="ab309-105">You can set the **Server** property at design time in the [RDS.DataControl](datacontrol-object-rds.md) object's OBJECT tags, or at run time in scripting code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab309-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ab309-106">Syntax</span></span>

|<span data-ttu-id="ab309-107">Protocolo</span><span class="sxs-lookup"><span data-stu-id="ab309-107">Protocol</span></span>|<span data-ttu-id="ab309-108">Sintaxe no tempo de design</span><span class="sxs-lookup"><span data-stu-id="ab309-108">Design-time syntax</span></span>|
|:-------|:-----------------|
|<span data-ttu-id="ab309-109">HTTP</span><span class="sxs-lookup"><span data-stu-id="ab309-109">HTTP</span></span>|`<PARAM NAME="Server" VALUE="https://awebsrvr:port">`|
|<span data-ttu-id="ab309-110">HTTPS</span><span class="sxs-lookup"><span data-stu-id="ab309-110">HTTPS</span></span>|`<PARAM NAME="Server" VALUE="https://awebsrvr:port">`|
|<span data-ttu-id="ab309-111">DCOM</span><span class="sxs-lookup"><span data-stu-id="ab309-111">DCOM</span></span>|`<PARAM NAME="Server" VALUE="computername">`|
|<span data-ttu-id="ab309-112">Em processo</span><span class="sxs-lookup"><span data-stu-id="ab309-112">In-process</span></span>|`<PARAM NAME="Server" VALUE="">`|


|<span data-ttu-id="ab309-113">Protocolo</span><span class="sxs-lookup"><span data-stu-id="ab309-113">Protocol</span></span>|<span data-ttu-id="ab309-114">Sintaxe em tempo de execução</span><span class="sxs-lookup"><span data-stu-id="ab309-114">Run-time syntax</span></span>|
|:-------|:--------------|
|<span data-ttu-id="ab309-115">HTTP</span><span class="sxs-lookup"><span data-stu-id="ab309-115">HTTP</span></span>|`DataControl.Server="https://awebsrvr:port"`|
|<span data-ttu-id="ab309-116">HTTPS</span><span class="sxs-lookup"><span data-stu-id="ab309-116">HTTPS</span></span>|`DataControl.Server="https://awebsrvr:port"`|
|<span data-ttu-id="ab309-117">DCOM</span><span class="sxs-lookup"><span data-stu-id="ab309-117">DCOM</span></span>|`DataControl.Server="computername"`|
|<span data-ttu-id="ab309-118">Em processo</span><span class="sxs-lookup"><span data-stu-id="ab309-118">In-process</span></span>|`DataControl.Server=""`|


## <a name="parameters"></a><span data-ttu-id="ab309-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ab309-119">Parameters</span></span>

<span data-ttu-id="ab309-120">*awebsrvr* ou *computername*</span><span class="sxs-lookup"><span data-stu-id="ab309-120">*awebsrvr* or *computername*</span></span>

- <span data-ttu-id="ab309-121">Um valor **String** que contém um caminho de Internet ou intranet, ou nome do computador, se o servidor estiver em um computador remoto; ou, uma cadeia de caracteres em branco, se o servidor estiver no computador local.</span><span class="sxs-lookup"><span data-stu-id="ab309-121">A **String** value that contains an Internet or intranet path, or computer name, if the server is on a remote computer; or, an empty string if the server is on the local computer.</span></span>

<span data-ttu-id="ab309-122">*porta*</span><span class="sxs-lookup"><span data-stu-id="ab309-122">*port*</span></span>

- <span data-ttu-id="ab309-p101">Opcional. Uma porta que é utilizada para conexão com um servidor IIS. O número da porta é definido no Internet Explorer (no menu **Exibir**, clique em **Opções** e selecione a guia **Conexões** ) ou no IIS.</span><span class="sxs-lookup"><span data-stu-id="ab309-p101">Optional. A port that is used to connect to an IIS server. The port number is set in Internet Explorer (on the **Tools** menu, click **Internet Options**, and then select the **Connection** tab) or in IIS.</span></span>

<span data-ttu-id="ab309-126">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="ab309-126">*DataControl*</span></span>

- <span data-ttu-id="ab309-127">Uma variável de objeto que representa um objeto **RDS.DataControl**.</span><span class="sxs-lookup"><span data-stu-id="ab309-127">An object variable that represents an **RDS.DataControl** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab309-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab309-128">Remarks</span></span>

<span data-ttu-id="ab309-129">O servidor é o local onde a solicitação de **RDS.DataControl** (isto é, uma consulta ou atualização) é processada.</span><span class="sxs-lookup"><span data-stu-id="ab309-129">The server is the location where the **RDS.DataControl** request (that is, a query or update) is processed.</span></span> <span data-ttu-id="ab309-130">Por padrão, todas as solicitações são processadas pelo objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md), pelo componente [ MSDFMAP.Handler ](datafactory-customization.md) e pelo arquivo [MSDFMAP.INI](understanding-the-customization-file.md) no servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="ab309-130">By default, all requests are processed by the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object, [MSDFMAP.Handler](datafactory-customization.md) component, and [MSDFMAP.INI](understanding-the-customization-file.md) file on the specified server.</span></span> 

<span data-ttu-id="ab309-131">Lembre-se de reconciliar as definições nos arquivos **MSDFMAP.INI** antigos e novos, quando alterar os servidores.</span><span class="sxs-lookup"><span data-stu-id="ab309-131">Remember that when changing servers to reconcile settings in the old and new **MSDFMAP.INI** files.</span></span> <span data-ttu-id="ab309-132">Incompatibilidades poderão fazer com que solicitações bem-sucedidas em um servidor, falhem em outro servidor.</span><span class="sxs-lookup"><span data-stu-id="ab309-132">Incompatibilities may cause requests that succeed on one server to fail on another.</span></span> <span data-ttu-id="ab309-133">Se a propriedade Server estiver definida como "", esses objetos serão utilizados na máquina local.</span><span class="sxs-lookup"><span data-stu-id="ab309-133">If the Server property is set to "", these objects will be used on the local machine.</span></span>

