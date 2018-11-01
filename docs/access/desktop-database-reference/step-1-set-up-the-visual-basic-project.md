---
title: 'Etapa 1: Configurar o projeto do Visual Basic'
TOCTitle: 'Step 1: Set Up the Visual Basic Project'
ms:assetid: 1b8195c9-60c8-18a2-3fa2-ffdeed370748
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248954(v=office.15)
ms:contentKeyID: 48543544
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 31b81c762f192f8a56e56baf0c5e0ae5b6b6fadf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868648"
---
# <a name="step-1-set-up-the-visual-basic-project"></a><span data-ttu-id="86b41-102">Etapa 1: Configurar o projeto do Visual Basic</span><span class="sxs-lookup"><span data-stu-id="86b41-102">Step 1: Set Up the Visual Basic Project</span></span>


<span data-ttu-id="86b41-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="86b41-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="step-1-set-up-the-visual-basic-project"></a><span data-ttu-id="86b41-104">Etapa 1: Configurar o projeto do Visual Basic</span><span class="sxs-lookup"><span data-stu-id="86b41-104">Step 1: Set Up the Visual Basic Project</span></span>

<span data-ttu-id="86b41-105">Neste cenário, considera-se que você tem o Microsoft Visual Basic 6.0 ou posterior, ADO 2.5 ou posterior e o Microsoft OLE DB Provider for Internet Publishing instalado no seu sistema.</span><span class="sxs-lookup"><span data-stu-id="86b41-105">In this scenario, it is assumed that you have Microsoft Visual Basic 6.0 or later, ADO 2.5 or later, and the Microsoft OLE DB Provider for Internet Publishing installed on your system.</span></span>

<span data-ttu-id="86b41-106">**Para criar um projeto ADO**</span><span class="sxs-lookup"><span data-stu-id="86b41-106">**To create an ADO project**</span></span>

1.  <span data-ttu-id="86b41-107">No Microsoft Visual Basic, crie um novo projeto EXE padrão.</span><span class="sxs-lookup"><span data-stu-id="86b41-107">In Microsoft Visual Basic, create a new Standard EXE project.</span></span>

2.  <span data-ttu-id="86b41-108">No menu **Projeto**, clique em **Referências**.</span><span class="sxs-lookup"><span data-stu-id="86b41-108">From the **Project** menu, choose **References**.</span></span>

3.  <span data-ttu-id="86b41-109">Selecione **"Biblioteca do Microsoft ActiveX Data Objects 2.5**" e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="86b41-109">Select **"Microsoft ActiveX Data Objects 2.5 Library**" and click **OK**.</span></span>

<span data-ttu-id="86b41-110">**Para inserir os controles no formulário principal**</span><span class="sxs-lookup"><span data-stu-id="86b41-110">**To insert controls on the main form**</span></span>

1.  <span data-ttu-id="86b41-p101">Adicione um controle ListBox em Form1. Defina a propriedade **Name** como lstMain.</span><span class="sxs-lookup"><span data-stu-id="86b41-p101">Add a ListBox control to Form1. Set its **Name** property to lstMain.</span></span>

2.  <span data-ttu-id="86b41-p102">Adicione outro controle ListBox em Form1. Defina a propriedade **Name** como lstDetails.</span><span class="sxs-lookup"><span data-stu-id="86b41-p102">Add another ListBox control to Form1. Set its **Name** property to lstDetails.</span></span>

3.  <span data-ttu-id="86b41-p103">Adicione um controle TextBox em Form1. Defina a propriedade **Name** como txtDetails.</span><span class="sxs-lookup"><span data-stu-id="86b41-p103">Add a TextBox control to Form1. Set its **Name** property to txtDetails.</span></span>

