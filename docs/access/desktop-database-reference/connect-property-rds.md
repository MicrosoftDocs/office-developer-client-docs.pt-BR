---
title: Propriedade Connect (RDS)
TOCTitle: Connect property (RDS)
ms:assetid: 11aa3284-18e9-6d2d-761b-c25090370b77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248890(v=office.15)
ms:contentKeyID: 48543324
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2b0d0969d9cbcf972a1b57faf27bbea1dfd960d5
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949415"
---
# <a name="connect-property-rds"></a><span data-ttu-id="b17c1-102">Propriedade Connect (RDS)</span><span class="sxs-lookup"><span data-stu-id="b17c1-102">Connect property (RDS)</span></span>

<span data-ttu-id="b17c1-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="b17c1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b17c1-104">Indica o nome do banco de dados a partir do qual são executadas as operações de consulta e atualização.</span><span class="sxs-lookup"><span data-stu-id="b17c1-104">Indicates the database name from which the query and update operations are run.</span></span>

<span data-ttu-id="b17c1-105">É possível definir a propriedade **Connect** em tempo de design nas marcas OBJECT do objeto [RDS.DataControl](datacontrol-object-rds.md) ou em tempo de execução no código de script (por exemplo, VBScript).</span><span class="sxs-lookup"><span data-stu-id="b17c1-105">You can set the **Connect** property at design time in the [RDS.DataControl](datacontrol-object-rds.md) object's OBJECT tags, or at run time in scripting code (for instance, VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="b17c1-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b17c1-106">Syntax</span></span>

<span data-ttu-id="b17c1-107">Tempo de design: \<nome do parâmetro = "Conectar" valor = "ConnectionString"\></span><span class="sxs-lookup"><span data-stu-id="b17c1-107">Design time: \<PARAM NAME="Connect" VALUE="ConnectionString"\></span></span>

<span data-ttu-id="b17c1-108">Tempo de execução: DataControl.Connect = "ConnectionString"</span><span class="sxs-lookup"><span data-stu-id="b17c1-108">Run time: DataControl.Connect = "ConnectionString"</span></span>

## <a name="parameters"></a><span data-ttu-id="b17c1-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b17c1-109">Parameters</span></span>

|<span data-ttu-id="b17c1-110">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="b17c1-110">Parameter</span></span>|<span data-ttu-id="b17c1-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="b17c1-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="b17c1-112">*ConnectionString*</span><span class="sxs-lookup"><span data-stu-id="b17c1-112">*ConnectionString*</span></span> |<span data-ttu-id="b17c1-p101">Uma sequência de conexão válida. Para obter mais informações gerais sobre sequências de conexão, consulte a propriedade [ConnectionString](connectionstring-property-ado.md) ou a documentação de seu provedor.</span><span class="sxs-lookup"><span data-stu-id="b17c1-p101">A valid connection string. For more general information about connection strings, see the [ConnectionString](connectionstring-property-ado.md) property or your provider documentation.</span></span><br/><br/><span data-ttu-id="b17c1-115">**Observação**: especificando MS Remote como o provedor para o **RDS. DataControl** criará um cenário de quatro camadas.</span><span class="sxs-lookup"><span data-stu-id="b17c1-115">**NOTE**: Specifying MS Remote as the provider for the **RDS.DataControl** would create a four-tier scenario.</span></span> <span data-ttu-id="b17c1-116">Cenários com mais de três camadas não foram testados e não devem ser necessários.</span><span class="sxs-lookup"><span data-stu-id="b17c1-116">Scenarios greater than three tiers have not been tested and should not be needed.</span></span>|
|<span data-ttu-id="b17c1-117">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="b17c1-117">*DataControl*</span></span> |<span data-ttu-id="b17c1-118">Uma variável de objeto que representa um objeto **RDS.DataControl**.</span><span class="sxs-lookup"><span data-stu-id="b17c1-118">An object variable that represents an **RDS.DataControl** object.</span></span>|

