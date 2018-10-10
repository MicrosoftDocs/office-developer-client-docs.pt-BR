---
title: Propriedade Connect (RDS)
TOCTitle: Connect Property (RDS)
ms:assetid: 11aa3284-18e9-6d2d-761b-c25090370b77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248890(v=office.15)
ms:contentKeyID: 48543324
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: eb628356e4d93201c38cf84a9c3245b13e044ee3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464706"
---
# <a name="connect-property-rds"></a><span data-ttu-id="3737d-102">Propriedade Connect (RDS)</span><span class="sxs-lookup"><span data-stu-id="3737d-102">Connect Property (RDS)</span></span>


<span data-ttu-id="3737d-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3737d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3737d-104">Indica o nome do banco de dados a partir do qual são executadas as operações de consulta e atualização.</span><span class="sxs-lookup"><span data-stu-id="3737d-104">Indicates the database name from which the query and update operations are run.</span></span>

<span data-ttu-id="3737d-105">É possível definir a propriedade **Connect** em tempo de design nas marcas OBJECT do objeto [RDS.DataControl](datacontrol-object-rds.md) ou em tempo de execução no código de script (por exemplo, VBScript).</span><span class="sxs-lookup"><span data-stu-id="3737d-105">You can set the **Connect** property at design time in the [RDS.DataControl](datacontrol-object-rds.md) object's OBJECT tags, or at run time in scripting code (for instance, VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="3737d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3737d-106">Syntax</span></span>

<span data-ttu-id="3737d-107">Tempo de design: \<nome do parâmetro = "Conectar" valor = "ConnectionString"\></span><span class="sxs-lookup"><span data-stu-id="3737d-107">Design time: \<PARAM NAME="Connect" VALUE="ConnectionString"\></span></span>

<span data-ttu-id="3737d-108">Tempo de execução: DataControl.Connect = "ConnectionString"</span><span class="sxs-lookup"><span data-stu-id="3737d-108">Run time: DataControl.Connect = "ConnectionString"</span></span>

## <a name="parameters"></a><span data-ttu-id="3737d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3737d-109">Parameters</span></span>

  - <span data-ttu-id="3737d-110">*ConnectionString*</span><span class="sxs-lookup"><span data-stu-id="3737d-110">*ConnectionString*</span></span>

  - <span data-ttu-id="3737d-p101">Uma sequência de conexão válida. Para obter mais informações gerais sobre sequências de conexão, consulte a propriedade [ConnectionString](connectionstring-property-ado.md) ou a documentação de seu provedor.</span><span class="sxs-lookup"><span data-stu-id="3737d-p101">A valid connection string. For more general information about connection strings, see the [ConnectionString](connectionstring-property-ado.md) property or your provider documentation.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="3737d-p102">[!OBSERVAçãO] A especificação do MS Remote como o provedor para o <STRONG>RDS.DataControl</STRONG> criaria um cenário de quatro camadas. Cenários com mais de três camadas não foram testados e não devem ser necessários.</span><span class="sxs-lookup"><span data-stu-id="3737d-p102">Specifying MS Remote as the provider for the <STRONG>RDS.DataControl</STRONG> would create a four-tier scenario. Scenarios greater than three tiers have not been tested and should not be needed.</span></span></P>



  - <span data-ttu-id="3737d-115">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="3737d-115">*DataControl*</span></span>

  - <span data-ttu-id="3737d-116">Uma variável de objeto que representa um objeto **RDS.DataControl**.</span><span class="sxs-lookup"><span data-stu-id="3737d-116">An object variable that represents an **RDS.DataControl** object.</span></span>

