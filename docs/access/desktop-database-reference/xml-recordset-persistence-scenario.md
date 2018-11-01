---
title: Cenário de persistência do Recordset XML
TOCTitle: XML Recordset Persistence Scenario
ms:assetid: 08f464da-10ba-b649-7571-766a40da2e04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248825(v=office.15)
ms:contentKeyID: 48543107
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fbf60cf8ef6099f8d16ab20f4441477fad1d32ab
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/01/2018
ms.locfileid: "25891167"
---
# <a name="xml-recordset-persistence-scenario"></a><span data-ttu-id="0ad89-102">Cenário de persistência do conjunto de registros do XML</span><span class="sxs-lookup"><span data-stu-id="0ad89-102">XML Recordset Persistence Scenario</span></span>

<span data-ttu-id="0ad89-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="0ad89-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="xml-recordset-persistence-scenario"></a><span data-ttu-id="0ad89-104">Cenário de persistência do conjunto de registros do XML</span><span class="sxs-lookup"><span data-stu-id="0ad89-104">XML Recordset Persistence Scenario</span></span>

<span data-ttu-id="0ad89-105">Neste cenário, você criará um aplicativo ASP (Active Server Pages) que salva o conteúdo de um objeto **Recordset** diretamente no objeto **Response** ASP.</span><span class="sxs-lookup"><span data-stu-id="0ad89-105">In this scenario, you will create an Active Server Pages (ASP) application that saves the contents of a **Recordset** object directly to the ASP **Response** object.</span></span>

> [!NOTE]
> <span data-ttu-id="0ad89-106">[!OBSERVAçãO] Este cenário exige que seu servidor tenha o IIS 5.0 (Internet Information Server) ou posterior instalado.</span><span class="sxs-lookup"><span data-stu-id="0ad89-106">This scenario requires that your server have Internet Information Server 5.0 (IIS) or later installed.</span></span>

<span data-ttu-id="0ad89-107">O **Recordset** retornado é exibido no Internet Explorer usando um [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="0ad89-107">The returned **Recordset** is displayed in Internet Explorer using an [RDS.DataControl](datacontrol-object-rds.md).</span></span>

<span data-ttu-id="0ad89-108">As seguintes etapas são necessárias para criar este cenário:</span><span class="sxs-lookup"><span data-stu-id="0ad89-108">The following steps are necessary to create this scenario:</span></span>

1.  <span data-ttu-id="0ad89-109">Configurar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0ad89-109">Set up the application.</span></span>

2.  <span data-ttu-id="0ad89-110">Obter os dados.</span><span class="sxs-lookup"><span data-stu-id="0ad89-110">Get the data.</span></span>

3.  <span data-ttu-id="0ad89-111">Enviar os dados.</span><span class="sxs-lookup"><span data-stu-id="0ad89-111">Send the data.</span></span>

4.  <span data-ttu-id="0ad89-112">Receber e exibir os dados.</span><span class="sxs-lookup"><span data-stu-id="0ad89-112">Receive and display the data.</span></span>

### <a name="next-step"></a><span data-ttu-id="0ad89-113">Próxima etapa</span><span class="sxs-lookup"><span data-stu-id="0ad89-113">Next step</span></span>

[<span data-ttu-id="0ad89-114">Etapa 1: Configurar o aplicativo</span><span class="sxs-lookup"><span data-stu-id="0ad89-114">Step 1: Set Up the Application</span></span>](step-1-set-up-the-application.md)

