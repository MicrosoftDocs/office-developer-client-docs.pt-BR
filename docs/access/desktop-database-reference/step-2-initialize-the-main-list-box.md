---
title: 'Etapa 2: Inicializar a caixa de listagem Principal'
TOCTitle: 'Step 2: Initialize the Main List Box'
ms:assetid: 81e4dcfd-6ee0-b5f9-9ea3-026c38c26bf0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249562(v=office.15)
ms:contentKeyID: 48545967
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3505c2726da3f2f2f01d179c97cde5a1d7b635ba
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869894"
---
# <a name="step-2-initialize-the-main-list-box"></a><span data-ttu-id="9d88c-102">Etapa 2: Inicializar a caixa de listagem Principal</span><span class="sxs-lookup"><span data-stu-id="9d88c-102">Step 2: Initialize the Main List Box</span></span>


<span data-ttu-id="9d88c-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="9d88c-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="step-2-initialize-the-main-list-box"></a><span data-ttu-id="9d88c-104">Etapa 2: Inicializar a caixa de listagem principal</span><span class="sxs-lookup"><span data-stu-id="9d88c-104">Step 2: Initialize the Main List Box</span></span>

<span data-ttu-id="9d88c-105">**Para declarar os objetos Record e Recordset globais**</span><span class="sxs-lookup"><span data-stu-id="9d88c-105">**To declare global Record and Recordset objects**</span></span>

  - <span data-ttu-id="9d88c-106">Insira o seguinte código em (General) (Declarations) para Form1:</span><span class="sxs-lookup"><span data-stu-id="9d88c-106">Insert the following code into the (General) (Declarations) for Form1:</span></span>
    
    ```vb 
     
    Option Explicit 
    Dim grec As Record 
    Dim grs As Recordset 
    ```
    
    <span data-ttu-id="9d88c-107">Este código declara as referências de objetos globais para os objetos **Record** e **Recordset** que serão usados posteriormente neste cenário.</span><span class="sxs-lookup"><span data-stu-id="9d88c-107">This code declares global object references for **Record** and **Recordset** objects that will be used later in this scenario.</span></span>

<span data-ttu-id="9d88c-108">**Para se conectar a um URL e preencher lstMain**</span><span class="sxs-lookup"><span data-stu-id="9d88c-108">**To connect to a URL and populate lstMain**</span></span>

  - <span data-ttu-id="9d88c-109">Insira o seguinte código no manipulador de eventos Form Load para Form1:</span><span class="sxs-lookup"><span data-stu-id="9d88c-109">Insert the following code into the Form Load event handler for Form1:</span></span>
    
    ```vb 
     
    Private Sub Form_Load() 
        Set grec = New Record 
        Set grs = New Recordset 
        grec.Open "", "URL=https://servername/foldername/", , _ 
            adOpenIfExists Or adCreateCollection 
        Set grs = grec.GetChildren 
        While Not grs.EOF 
            lstMain.AddItem grs(0) 
            grs.MoveNext 
        Wend 
    End Sub 
    ```
    
    <span data-ttu-id="9d88c-110">Este código instancia os objetos **Record** e **Recordset** globais.</span><span class="sxs-lookup"><span data-stu-id="9d88c-110">This code instantiates the global **Record** and **Recordset** objects.</span></span> <span data-ttu-id="9d88c-111">O **registro**, grec, é aberto com uma URL especificada como o **ActiveConnection**.</span><span class="sxs-lookup"><span data-stu-id="9d88c-111">The **Record**, grec, is opened with a URL specified as the **ActiveConnection**.</span></span> <span data-ttu-id="9d88c-112">Se o URL existir, estará aberto; se ainda não existir, será criado.</span><span class="sxs-lookup"><span data-stu-id="9d88c-112">If the URL exists, it is opened; if it does not already exist, it is created.</span></span> <span data-ttu-id="9d88c-113">Observe que você deveria substituir "https://servername/foldername/" por um URL válido a partir do seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="9d88c-113">Note that you should replace "https://servername/foldername/" with a valid URL from your environment.</span></span> <span data-ttu-id="9d88c-114">O **Recordset**, grs, é aberto nos filhos do **registro**, grec.</span><span class="sxs-lookup"><span data-stu-id="9d88c-114">The **Recordset**, grs, is opened on the children of the **Record**, grec.</span></span> <span data-ttu-id="9d88c-115">Em seguida, lstMain é preenchido com os nomes dos arquivos dos recursos publicados no URL.</span><span class="sxs-lookup"><span data-stu-id="9d88c-115">Then lstMain is populated with the file names of the resources published to the URL.</span></span>

