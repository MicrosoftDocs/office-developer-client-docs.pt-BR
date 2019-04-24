---
title: Propriedade Connect (RDS)
TOCTitle: Connect property (RDS)
ms:assetid: 11aa3284-18e9-6d2d-761b-c25090370b77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248890(v=office.15)
ms:contentKeyID: 48543324
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 42e7dd643985cee9aef8887099eb90dcdb381f4e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295979"
---
# <a name="connect-property-rds"></a><span data-ttu-id="72242-102">Propriedade Connect (RDS)</span><span class="sxs-lookup"><span data-stu-id="72242-102">Connect property (RDS)</span></span>

<span data-ttu-id="72242-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="72242-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="72242-104">Indica o nome do banco de dados a partir do qual são executadas as operações de consulta e atualização.</span><span class="sxs-lookup"><span data-stu-id="72242-104">Indicates the database name from which the query and update operations are run.</span></span>

<span data-ttu-id="72242-105">É possível definir a propriedade **Connect** em tempo de design nas marcas OBJECT do objeto [RDS.DataControl](datacontrol-object-rds.md) ou em tempo de execução no código de script (por exemplo, VBScript).</span><span class="sxs-lookup"><span data-stu-id="72242-105">You can set the **Connect** property at design time in the [RDS.DataControl](datacontrol-object-rds.md) object's OBJECT tags, or at run time in scripting code (for instance, VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="72242-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="72242-106">Syntax</span></span>

<span data-ttu-id="72242-107">Tempo de design \<: parâmetro Name = "Connect" value = "ConnectionString"\></span><span class="sxs-lookup"><span data-stu-id="72242-107">Design time: \<PARAM NAME="Connect" VALUE="ConnectionString"\></span></span>

<span data-ttu-id="72242-108">Tempo de execução: dataControl. Connect = "ConnectionString"</span><span class="sxs-lookup"><span data-stu-id="72242-108">Run time: DataControl.Connect = "ConnectionString"</span></span>

## <a name="parameters"></a><span data-ttu-id="72242-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="72242-109">Parameters</span></span>

|<span data-ttu-id="72242-110">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="72242-110">Parameter</span></span>|<span data-ttu-id="72242-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="72242-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="72242-112">*ConnectionString*</span><span class="sxs-lookup"><span data-stu-id="72242-112">*ConnectionString*</span></span> |<span data-ttu-id="72242-p101">Uma sequência de conexão válida. Para obter mais informações gerais sobre sequências de conexão, consulte a propriedade [ConnectionString](connectionstring-property-ado.md) ou a documentação de seu provedor.</span><span class="sxs-lookup"><span data-stu-id="72242-p101">A valid connection string. For more general information about connection strings, see the [ConnectionString](connectionstring-property-ado.md) property or your provider documentation.</span></span><br/><br/><span data-ttu-id="72242-115">**Observação**: ESPECIFICANDO o MS Remote como o provedor para o **RDS. DataControl** criaria um cenário de quatro camadas.</span><span class="sxs-lookup"><span data-stu-id="72242-115">**NOTE**: Specifying MS Remote as the provider for the **RDS.DataControl** would create a four-tier scenario.</span></span> <span data-ttu-id="72242-116">Cenários com mais de três camadas não foram testados e não devem ser necessários.</span><span class="sxs-lookup"><span data-stu-id="72242-116">Scenarios greater than three tiers have not been tested and should not be needed.</span></span>|
|<span data-ttu-id="72242-117">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="72242-117">*DataControl*</span></span> |<span data-ttu-id="72242-118">Uma variável de objeto que representa um objeto **RDS.DataControl**.</span><span class="sxs-lookup"><span data-stu-id="72242-118">An object variable that represents an **RDS.DataControl** object.</span></span>|

