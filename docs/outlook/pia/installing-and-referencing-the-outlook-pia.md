---
title: Instalar e fazer referência ao Outlook PIA
TOCTitle: Installing and referencing the Outlook PIA
ms:assetid: b1afd047-dcbb-480f-ba74-993d7d7114cb
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb646840(v=office.15)
ms:contentKeyID: 55119774
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 45584ae0a7050aa769368db518c9efcd5db9975a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336873"
---
# <a name="installing-and-referencing-the-outlook-pia"></a><span data-ttu-id="36371-102">Instalar e fazer referência ao Outlook PIA</span><span class="sxs-lookup"><span data-stu-id="36371-102">Installing and referencing the Outlook PIA</span></span>

<span data-ttu-id="36371-103">O Assembly de Interoperabilidade Primário (PIA) do Outlook deve estar instalado no Cache de Assembly Global (GAC) antes de poder incorporar informações do PIA a um suplemento gerenciado do Outlook.</span><span class="sxs-lookup"><span data-stu-id="36371-103">You must have the Outlook Primary Interop Assembly (PIA) installed in the Global Assembly Cache (GAC) before you can incorporate information from the PIA in an Outlook managed add-in.</span></span> <span data-ttu-id="36371-104">Por padrão, o PIA é instalado automaticamente quando você instala o Office no computador de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="36371-104">By default, the PIA is installed automatically when you install Office on the development computer.</span></span> <span data-ttu-id="36371-105">No entanto, se você precisar instalar o PIA separadamente, confira [Configurar o computador para desenvolver soluções do Office](https://docs.microsoft.com/visualstudio/vsto/configuring-a-computer-to-develop-office-solutions?view=vs-2017).</span><span class="sxs-lookup"><span data-stu-id="36371-105">However, if you need to install the PIA separately, see [Configure a computer to develop Office solutions](https://docs.microsoft.com/visualstudio/vsto/configuring-a-computer-to-develop-office-solutions?view=vs-2017).</span></span>


> [!NOTE] 
> <span data-ttu-id="36371-106">Você deve ser um administrador no computador de desenvolvimento para instalar os PIAs do Office.</span><span class="sxs-lookup"><span data-stu-id="36371-106">You must be an administrator on the development computer to install the Office PIAs.</span></span>

<span data-ttu-id="36371-107">Após a instalação, se você estiver usando o Visual Studio para criar o projeto gerenciado, adicione uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0.</span><span class="sxs-lookup"><span data-stu-id="36371-107">After installation, if you are using Visual Studio to create the managed project, you can add a reference to the Microsoft Outlook 15.0 Object Library component.</span></span> <span data-ttu-id="36371-108">Subsequentemente, no navegador de objetos, no namespace **Microsoft.Office.Interop.Outlook**, você pode ver interfaces gerenciadas no PIA com nomes correspondentes a objetos no modelo de objeto do Outlook.</span><span class="sxs-lookup"><span data-stu-id="36371-108">Subsequently, in the object browser, under the **Microsoft.Office.Interop.Outlook** namespace, you can see managed interfaces in the PIA that have names corresponding to objects in the Outlook object model.</span></span>

## <a name="see-also"></a><span data-ttu-id="36371-109">Confira também</span><span class="sxs-lookup"><span data-stu-id="36371-109">See also</span></span>

- [<span data-ttu-id="36371-110">Instalar assemblies de interoperabilidade primários do Office</span><span class="sxs-lookup"><span data-stu-id="36371-110">Install Office primary interop assemblies</span></span>](https://docs.microsoft.com/visualstudio/vsto/how-to-install-office-primary-interop-assemblies?view=vs-2017)
- [<span data-ttu-id="36371-111">Arquitetura do Outlook PIA</span><span class="sxs-lookup"><span data-stu-id="36371-111">Architecture of the Outlook PIA</span></span>](architecture-of-the-outlook-pia.md)

