---
title: Usando XSLT personalizado em modelos de formulário do InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 32c80bcd-a5d6-af32-38ba-9ca9ff148b99
description: Você pode criar a maior parte dos elementos de exibição que provavelmente precisará no designer de formulários do Microsoft InfoPath. No entanto, se você precisar de um elemento de exibição personalizado que o InfoPath não possa criar para você, poderá modificar manualmente a transformação em XSL (XSLT) que o InfoPath usa para gerar o modo de exibição. Para fazer isso, extraia o formulário em seus arquivos de componente usando exportar arquivos de origem na guia publicar do Microsoft Office Backstage e edite a transformação no editor de XML preferencial, como Microsoft Visual Studio ou bloco de notas.
ms.openlocfilehash: a61980191dbedeec33b06ad8173ce50126fea781
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428267"
---
# <a name="using-custom-xslt-in-infopath-form-templates"></a><span data-ttu-id="3a06f-105">Usando XSLT personalizado em modelos de formulário do InfoPath</span><span class="sxs-lookup"><span data-stu-id="3a06f-105">Using Custom XSLT in InfoPath Form Templates</span></span>

<span data-ttu-id="3a06f-106">Você pode criar a maior parte dos elementos de exibição que provavelmente precisará no designer de formulários do Microsoft InfoPath.</span><span class="sxs-lookup"><span data-stu-id="3a06f-106">You can create most of the view elements you're likely to need in the Microsoft InfoPath form designer.</span></span> <span data-ttu-id="3a06f-107">No entanto, se você precisar de um elemento de exibição personalizado que o InfoPath não possa criar para você, poderá modificar manualmente a transformação em XSL (XSLT) que o InfoPath usa para gerar o modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="3a06f-107">If you need a custom view element that InfoPath can't create for you, however, you can manually modify the XSL Transformation (XSLT) that InfoPath uses to generate the view.</span></span> <span data-ttu-id="3a06f-108">Para fazer isso, extraia o formulário em seus arquivos de componente usando **exportar arquivos de origem** na guia **publicar** do Microsoft Office Backstage e edite a transformação no editor de XML preferencial, como Microsoft Visual Studio ou bloco de notas.</span><span class="sxs-lookup"><span data-stu-id="3a06f-108">To do so, extract the form into its component files by using **Export Source Files** on the **Publish** tab of the Microsoft Office Backstage, and then edit the transform in your preferred XML editor, such as Microsoft Visual Studio or Notepad.</span></span> 
  
<span data-ttu-id="3a06f-109">Se você fizer alterações em uma transformação de exibição fora do InfoPath e, em seguida, abrir o modo de exibição no modo de design e fizer alterações, o InfoPath substituirá as alterações feitas manualmente.</span><span class="sxs-lookup"><span data-stu-id="3a06f-109">If you make changes to a view transform outside of InfoPath and then open the view in design mode and make changes, InfoPath will overwrite the changes you made manually.</span></span> <span data-ttu-id="3a06f-110">Para impedir que o InfoPath substitua as alterações feitas, você deve colocar essas alterações em um `<xsl:template>` elemento na transformação e usar o `xd:preserve` modo, conforme mostrado aqui:</span><span class="sxs-lookup"><span data-stu-id="3a06f-110">To keep InfoPath from overwriting the changes you make, you must place those changes in an  `<xsl:template>` element in the transform and use the  `xd:preserve` mode, as shown here:</span></span> 
  
```XML
<xsl:template match="my:field1" mode="xd:preserve"> 
   <div> 
      The value of field1 is <xsl:value-of select="."/> 
   </div> 
</xsl:template>
```

<span data-ttu-id="3a06f-111">Para incluir o modelo no arquivo transformado, use `<xsl:apply-templates>` o elemento com o `xd:preserve` mesmo modo:</span><span class="sxs-lookup"><span data-stu-id="3a06f-111">To include the template in the transformed file, use the  `<xsl:apply-templates>` element with the same  `xd:preserve` mode:</span></span> 
  
```XML
<xsl:apply-templates select="my:field1" mode="xd:preserve"/>
```

<span data-ttu-id="3a06f-112">Elementos e construções definidos em modelos XSL com o `xd:preserve` modo não serão exibidos no ambiente de design do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="3a06f-112">Elements and constructs defined within XSL templates with the  `xd:preserve` mode will not be displayed in the InfoPath design environment.</span></span> <span data-ttu-id="3a06f-113">Em vez disso, o InfoPath marcará a seção personalizada com um controle rotulado como **preservar bloco de código** com uma borda vermelha.</span><span class="sxs-lookup"><span data-stu-id="3a06f-113">Instead, InfoPath will mark the custom section with a control labeled **Preserve Code Block** with a red border.</span></span> <span data-ttu-id="3a06f-114">Quando um usuário abre o formulário para preenchê-lo, as transformações XSL personalizadas são aplicadas e os controles de **preservar bloco de código** não serão exibidos.</span><span class="sxs-lookup"><span data-stu-id="3a06f-114">When a user opens the form to fill it out, the custom XSL transforms are applied and the **Preserve Code Block** controls will not appear.</span></span> 
  

