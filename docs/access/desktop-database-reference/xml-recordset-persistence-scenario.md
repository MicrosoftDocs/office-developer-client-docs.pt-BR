---
title: Cenário de persistência do Recordset XML
TOCTitle: XML Recordset Persistence Scenario
ms:assetid: 08f464da-10ba-b649-7571-766a40da2e04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248825(v=office.15)
ms:contentKeyID: 48543107
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 378d3b1fc559cc07c1eb3a58621a8a4bd09a06ab
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861818"
---
# <a name="xml-recordset-persistence-scenario"></a><span data-ttu-id="1f569-102">Cenário de persistência do conjunto de registros do XML</span><span class="sxs-lookup"><span data-stu-id="1f569-102">XML Recordset Persistence Scenario</span></span>

<span data-ttu-id="1f569-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1f569-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="xml-recordset-persistence-scenario"></a><span data-ttu-id="1f569-104">Cenário de persistência do conjunto de registros do XML</span><span class="sxs-lookup"><span data-stu-id="1f569-104">XML Recordset Persistence Scenario</span></span>

<span data-ttu-id="1f569-105">Neste cenário, você criará um aplicativo ASP (Active Server Pages) que salva o conteúdo de um objeto **Recordset** diretamente no objeto **Response** ASP.</span><span class="sxs-lookup"><span data-stu-id="1f569-105">In this scenario, you will create an Active Server Pages (ASP) application that saves the contents of a **Recordset** object directly to the ASP **Response** object.</span></span>

> [!NOTE]
> <span data-ttu-id="1f569-106">[!OBSERVAçãO] Este cenário exige que seu servidor tenha o IIS 5.0 (Internet Information Server) ou posterior instalado.</span><span class="sxs-lookup"><span data-stu-id="1f569-106">This scenario requires that your server have Internet Information Server 5.0 (IIS) or later installed.</span></span>

<span data-ttu-id="1f569-107">O **Recordset** retornado é exibido no Internet Explorer usando um [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="1f569-107">The returned **Recordset** is displayed in Internet Explorer using an [RDS.DataControl](datacontrol-object-rds.md).</span></span>

<span data-ttu-id="1f569-108">As seguintes etapas são necessárias para criar este cenário:</span><span class="sxs-lookup"><span data-stu-id="1f569-108">The following steps are necessary to create this scenario:</span></span>

1.  <span data-ttu-id="1f569-109">Configurar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1f569-109">Set up the application.</span></span>

2.  <span data-ttu-id="1f569-110">Obter os dados.</span><span class="sxs-lookup"><span data-stu-id="1f569-110">Get the data.</span></span>

3.  <span data-ttu-id="1f569-111">Enviar os dados.</span><span class="sxs-lookup"><span data-stu-id="1f569-111">Send the data.</span></span>

4.  <span data-ttu-id="1f569-112">Receber e exibir os dados.</span><span class="sxs-lookup"><span data-stu-id="1f569-112">Receive and display the data.</span></span>

### <a name="next-step"></a><span data-ttu-id="1f569-113">Próxima etapa</span><span class="sxs-lookup"><span data-stu-id="1f569-113">Next step</span></span>

[<span data-ttu-id="1f569-114">Etapa 1: Configurar o aplicativo</span><span class="sxs-lookup"><span data-stu-id="1f569-114">Step 1: Set Up the Application</span></span>](step-1-set-up-the-application.md)

