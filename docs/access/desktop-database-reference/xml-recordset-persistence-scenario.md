---
title: Cenário de persistência do Recordset XML
TOCTitle: XML Recordset Persistence Scenario
ms:assetid: 08f464da-10ba-b649-7571-766a40da2e04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248825(v=office.15)
ms:contentKeyID: 48543107
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2bbb8a3aa50027be7ce025a04d5987a45fee888f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464820"
---
# <a name="xml-recordset-persistence-scenario"></a><span data-ttu-id="ab351-102">Cenário de persistência do Recordset XML</span><span class="sxs-lookup"><span data-stu-id="ab351-102">XML Recordset Persistence Scenario</span></span>


<span data-ttu-id="ab351-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ab351-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="xml-recordset-persistence-scenario"></a><span data-ttu-id="ab351-104">Cenário de persistência do Recordset XML</span><span class="sxs-lookup"><span data-stu-id="ab351-104">XML Recordset Persistence Scenario</span></span>

<span data-ttu-id="ab351-105">Neste cenário, você criará um aplicativo ASP (Active Server Pages) que salva o conteúdo de um objeto **Recordset** diretamente no objeto **Response** ASP.</span><span class="sxs-lookup"><span data-stu-id="ab351-105">In this scenario, you will create an Active Server Pages (ASP) application that saves the contents of a **Recordset** object directly to the ASP **Response** object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="ab351-106">[!OBSERVAçãO] Este cenário exige que seu servidor tenha o IIS 5.0 (Internet Information Server) ou posterior instalado.</span><span class="sxs-lookup"><span data-stu-id="ab351-106">This scenario requires that your server have Internet Information Server 5.0 (IIS) or later installed.</span></span></P>



<span data-ttu-id="ab351-107">O **Recordset** retornado é exibido no Internet Explorer usando um [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="ab351-107">The returned **Recordset** is displayed in Internet Explorer using an [RDS.DataControl](datacontrol-object-rds.md).</span></span>

<span data-ttu-id="ab351-108">As seguintes etapas são necessárias para criar este cenário:</span><span class="sxs-lookup"><span data-stu-id="ab351-108">The following steps are necessary to create this scenario:</span></span>

1.  <span data-ttu-id="ab351-109">Configurar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ab351-109">Set up the application.</span></span>

2.  <span data-ttu-id="ab351-110">Obter os dados.</span><span class="sxs-lookup"><span data-stu-id="ab351-110">Get the data.</span></span>

3.  <span data-ttu-id="ab351-111">Enviar os dados.</span><span class="sxs-lookup"><span data-stu-id="ab351-111">Send the data.</span></span>

4.  <span data-ttu-id="ab351-112">Receber e exibir os dados.</span><span class="sxs-lookup"><span data-stu-id="ab351-112">Receive and display the data.</span></span>

<span data-ttu-id="ab351-113">**Avançar**[Etapa 1: Configurar o aplicativo](step-1-set-up-the-application.md)</span><span class="sxs-lookup"><span data-stu-id="ab351-113">**Next**[Step 1: Set Up the Application](step-1-set-up-the-application.md)</span></span>

