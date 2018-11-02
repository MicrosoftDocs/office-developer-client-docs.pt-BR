---
title: Propriedade Connect (RDS)
TOCTitle: Connect property (RDS)
ms:assetid: 11aa3284-18e9-6d2d-761b-c25090370b77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248890(v=office.15)
ms:contentKeyID: 48543324
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ebd9eb25e2e0e6b9b2233ff0d9faf8c3e369f0f9
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925258"
---
# <a name="connect-property-rds"></a><span data-ttu-id="5203c-102">Propriedade Connect (RDS)</span><span class="sxs-lookup"><span data-stu-id="5203c-102">Connect property (RDS)</span></span>


<span data-ttu-id="5203c-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="5203c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5203c-104">Indica o nome do banco de dados a partir do qual são executadas as operações de consulta e atualização.</span><span class="sxs-lookup"><span data-stu-id="5203c-104">Indicates the database name from which the query and update operations are run.</span></span>

<span data-ttu-id="5203c-105">É possível definir a propriedade **Connect** em tempo de design nas marcas OBJECT do objeto [RDS.DataControl](datacontrol-object-rds.md) ou em tempo de execução no código de script (por exemplo, VBScript).</span><span class="sxs-lookup"><span data-stu-id="5203c-105">You can set the **Connect** property at design time in the [RDS.DataControl](datacontrol-object-rds.md) object's OBJECT tags, or at run time in scripting code (for instance, VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="5203c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5203c-106">Syntax</span></span>

<span data-ttu-id="5203c-107">Tempo de design: \<nome do parâmetro = "Conectar" valor = "ConnectionString"\></span><span class="sxs-lookup"><span data-stu-id="5203c-107">Design time: \<PARAM NAME="Connect" VALUE="ConnectionString"\></span></span>

<span data-ttu-id="5203c-108">Tempo de execução: DataControl.Connect = "ConnectionString"</span><span class="sxs-lookup"><span data-stu-id="5203c-108">Run time: DataControl.Connect = "ConnectionString"</span></span>

## <a name="parameters"></a><span data-ttu-id="5203c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5203c-109">Parameters</span></span>

- <span data-ttu-id="5203c-110">*ConnectionString*</span><span class="sxs-lookup"><span data-stu-id="5203c-110">*ConnectionString*</span></span>

  - <span data-ttu-id="5203c-p101">Uma sequência de conexão válida. Para obter mais informações gerais sobre sequências de conexão, consulte a propriedade [ConnectionString](connectionstring-property-ado.md) ou a documentação de seu provedor.</span><span class="sxs-lookup"><span data-stu-id="5203c-p101">A valid connection string. For more general information about connection strings, see the [ConnectionString](connectionstring-property-ado.md) property or your provider documentation.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="5203c-p102">[!OBSERVAçãO] A especificação do MS Remote como o provedor para o **RDS.DataControl** criaria um cenário de quatro camadas. Cenários com mais de três camadas não foram testados e não devem ser necessários.</span><span class="sxs-lookup"><span data-stu-id="5203c-p102">Specifying MS Remote as the provider for the **RDS.DataControl** would create a four-tier scenario. Scenarios greater than three tiers have not been tested and should not be needed.</span></span>

- <span data-ttu-id="5203c-115">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="5203c-115">*DataControl*</span></span>

  - <span data-ttu-id="5203c-116">Uma variável de objeto que representa um objeto **RDS.DataControl**.</span><span class="sxs-lookup"><span data-stu-id="5203c-116">An object variable that represents an **RDS.DataControl** object.</span></span>

