---
title: 'Etapa 5: O DataControl torna-se utilizável (Tutorial RDS)'
TOCTitle: 'Step 5: DataControl is Made Usable (RDS Tutorial)'
ms:assetid: 9eff5732-2743-6891-dfa6-0991645e17ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249728(v=office.15)
ms:contentKeyID: 48546672
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1d5b0dfef4d14594c2b2a9b8b57b866e032a07a5
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605650"
---
# <a name="step-5-datacontrol-is-made-usable-rds-tutorial"></a><span data-ttu-id="5d97f-102">Etapa 5: O DataControl torna-se utilizável (Tutorial RDS)</span><span class="sxs-lookup"><span data-stu-id="5d97f-102">Step 5: DataControl is Made Usable (RDS Tutorial)</span></span>


<span data-ttu-id="5d97f-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5d97f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5d97f-p101">O objeto **Recordset** retornado está disponível para uso. Você pode examinar, navegar ou editá-lo como faria com qualquer outro **Recordset**. As possibilidades de uso do **Recordset** dependem do seu ambiente. O Visual Basic e o Visual C++ possuem controles visuais que podem utilizar um **Recordset** diretamente ou indiretamente com a ajuda de um controle de dados de ativação.</span><span class="sxs-lookup"><span data-stu-id="5d97f-p101">The returned **Recordset** object is available for use. You can examine, navigate, or edit it as you would any other **Recordset**. What you can do with the **Recordset** depends on your environment. Visual Basic and Visual C++ have visual controls that can use a **Recordset** directly or indirectly with the aid of an enabling data control.</span></span>

<span data-ttu-id="5d97f-108"><<<<<<< Cabeça por exemplo, se você estiver exibindo uma página da Web no Microsoft Internet Explorer, você talvez queira exibir os dados do objeto **Recordset** em um controle visual.</span><span class="sxs-lookup"><span data-stu-id="5d97f-108"><<<<<<< HEAD For example, if you are displaying a Web page in Microsoft Internet Explorer, you might want to display the **Recordset** object data in a visual control.</span></span> <span data-ttu-id="5d97f-109">Os controles visuais em uma página da Web não podem acessar um objeto **Recordset** diretamente.</span><span class="sxs-lookup"><span data-stu-id="5d97f-109">Visual controls on a Web page cannot access a **Recordset** object directly.</span></span> <span data-ttu-id="5d97f-110">No entanto, podem acessar o objeto **Recordset** através do [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="5d97f-110">However, they can access the **Recordset** object through the [RDS.DataControl](datacontrol-object-rds.md).</span></span> <span data-ttu-id="5d97f-111">O **RDS.DataControl** torna-se utilizável por um controle visual quando sua propriedade [SourceRecordset](recordset-sourcerecordset-properties-rds.md) for definida como o objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="5d97f-111">The **RDS.DataControl** becomes usable by a visual control when its [SourceRecordset](recordset-sourcerecordset-properties-rds.md) property is set to the **Recordset** object.</span></span>
<span data-ttu-id="5d97f-112">=== Por exemplo, se você está exibindo uma página da Web no Microsoft Internet Explorer, você deseja exibir os dados do objeto **Recordset** em um controle visual.</span><span class="sxs-lookup"><span data-stu-id="5d97f-112">======= For example, if you are displaying a webpage in Microsoft Internet Explorer, you might want to display the **Recordset** object data in a visual control.</span></span> <span data-ttu-id="5d97f-113">Controles visuais em uma página da Web não podem acessar um objeto **Recordset** diretamente.</span><span class="sxs-lookup"><span data-stu-id="5d97f-113">Visual controls on a webpage cannot access a **Recordset** object directly.</span></span> <span data-ttu-id="5d97f-114">No entanto, podem acessar o objeto **Recordset** através do [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="5d97f-114">However, they can access the **Recordset** object through the [RDS.DataControl](datacontrol-object-rds.md).</span></span> <span data-ttu-id="5d97f-115">O **RDS.DataControl** torna-se utilizável por um controle visual quando sua propriedade [SourceRecordset](recordset-sourcerecordset-properties-rds.md) for definida como o objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="5d97f-115">The **RDS.DataControl** becomes usable by a visual control when its [SourceRecordset](recordset-sourcerecordset-properties-rds.md) property is set to the **Recordset** object.</span></span>
>>>>>>> <span data-ttu-id="5d97f-116">mestre</span><span class="sxs-lookup"><span data-stu-id="5d97f-116">master</span></span>

<span data-ttu-id="5d97f-117">O objeto de controle visual deve ter seu parâmetro **DATASRC** definido como **RDS.DataControl** e sua propriedade **DATAFLD** definida como um campo de objeto **Recordset** (coluna).</span><span class="sxs-lookup"><span data-stu-id="5d97f-117">The visual control object must have its **DATASRC** parameter set to the **RDS.DataControl**, and its **DATAFLD** property set to a **Recordset** object field (column).</span></span>

<span data-ttu-id="5d97f-118">Nesse tutorial, defina a propriedade **SourceRecordset**:</span><span class="sxs-lookup"><span data-stu-id="5d97f-118">In this tutorial, set the **SourceRecordset** property:</span></span>

```vb 
 
Sub RDSTutorial5() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DC as New RDS.DataControl 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
 DC.SourceRecordset = RS ' Visual controls can now bind to DC. 
... 
```

