---
title: 'Etapa 5: O DataControl torna-se utilizável (Tutorial RDS)'
TOCTitle: 'Step 5: DataControl is Made Usable (RDS Tutorial)'
ms:assetid: 9eff5732-2743-6891-dfa6-0991645e17ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249728(v=office.15)
ms:contentKeyID: 48546672
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1d9bd24d0aff1134a6af77862fd8f011d4ddff9f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464732"
---
# <a name="step-5-datacontrol-is-made-usable-rds-tutorial"></a><span data-ttu-id="2f96b-102">Etapa 5: O DataControl torna-se utilizável (Tutorial RDS)</span><span class="sxs-lookup"><span data-stu-id="2f96b-102">Step 5: DataControl is Made Usable (RDS Tutorial)</span></span>


<span data-ttu-id="2f96b-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2f96b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2f96b-p101">O objeto **Recordset** retornado está disponível para uso. Você pode examinar, navegar ou editá-lo como faria com qualquer outro **Recordset**. As possibilidades de uso do **Recordset** dependem do seu ambiente. O Visual Basic e o Visual C++ possuem controles visuais que podem utilizar um **Recordset** diretamente ou indiretamente com a ajuda de um controle de dados de ativação.</span><span class="sxs-lookup"><span data-stu-id="2f96b-p101">The returned **Recordset** object is available for use. You can examine, navigate, or edit it as you would any other **Recordset**. What you can do with the **Recordset** depends on your environment. Visual Basic and Visual C++ have visual controls that can use a **Recordset** directly or indirectly with the aid of an enabling data control.</span></span>

<span data-ttu-id="2f96b-p102">Por exemplo, se você estiver exibindo uma página da Web no Microsoft Internet Explorer, talvez queira exibir os dados de objeto **Recordset** em um controle visual. Os controles visuais em uma página da Web não podem acessar um objeto **Recordset** diretamente. No entanto, podem acessar o objeto **Recordset** através do [RDS.DataControl](datacontrol-object-rds.md). O **RDS.DataControl** torna-se utilizável por um controle visual quando sua propriedade [SourceRecordset](recordset-sourcerecordset-properties-rds.md) for definida como o objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="2f96b-p102">For example, if you are displaying a Web page in Microsoft Internet Explorer, you might want to display the **Recordset** object data in a visual control. Visual controls on a Web page cannot access a **Recordset** object directly. However, they can access the **Recordset** object through the [RDS.DataControl](datacontrol-object-rds.md). The **RDS.DataControl** becomes usable by a visual control when its [SourceRecordset](recordset-sourcerecordset-properties-rds.md) property is set to the **Recordset** object.</span></span>

<span data-ttu-id="2f96b-112">O objeto de controle visual deve ter seu parâmetro **DATASRC** definido como **RDS.DataControl** e sua propriedade **DATAFLD** definida como um campo de objeto **Recordset** (coluna).</span><span class="sxs-lookup"><span data-stu-id="2f96b-112">The visual control object must have its **DATASRC** parameter set to the **RDS.DataControl**, and its **DATAFLD** property set to a **Recordset** object field (column).</span></span>

<span data-ttu-id="2f96b-113">Nesse tutorial, defina a propriedade **SourceRecordset**:</span><span class="sxs-lookup"><span data-stu-id="2f96b-113">In this tutorial, set the **SourceRecordset** property:</span></span>

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

