---
title: Usar o XSLT personalizado em modelos de formulário do InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 32c80bcd-a5d6-af32-38ba-9ca9ff148b99
description: Você pode criar a maioria dos elementos de modo de exibição, que você provavelmente precisa no Microsoft InfoPath form designer. Se você precisar de um elemento de exibição personalizada que InfoPath não pode criar para você, no entanto, você pode modificar manualmente o XSL Transformation (XSLT) que usa o InfoPath para gerar o modo de exibição. Para fazer isso, extrair o formulário em seus arquivos de componente usando exportar os arquivos de origem na guia Publicar do Microsoft Office Backstage e editar a transformação no seu editor XML preferido, como o bloco de notas ou o Microsoft Visual Studio.
ms.openlocfilehash: 796115c99c81fc2a77812d91d317f5ce9ed54e5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765716"
---
# <a name="using-custom-xslt-in-infopath-form-templates"></a><span data-ttu-id="55216-105">Usar o XSLT personalizado em modelos de formulário do InfoPath</span><span class="sxs-lookup"><span data-stu-id="55216-105">Using Custom XSLT in InfoPath Form Templates</span></span>

<span data-ttu-id="55216-106">Você pode criar a maioria dos elementos de modo de exibição, que você provavelmente precisa no Microsoft InfoPath form designer.</span><span class="sxs-lookup"><span data-stu-id="55216-106">You can create most of the view elements you're likely to need in the Microsoft InfoPath form designer.</span></span> <span data-ttu-id="55216-107">Se você precisar de um elemento de exibição personalizada que InfoPath não pode criar para você, no entanto, você pode modificar manualmente o XSL Transformation (XSLT) que usa o InfoPath para gerar o modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="55216-107">If you need a custom view element that InfoPath can't create for you, however, you can manually modify the XSL Transformation (XSLT) that InfoPath uses to generate the view.</span></span> <span data-ttu-id="55216-108">Para fazer isso, extrair o formulário em seus arquivos de componente usando **Exportar arquivos de origem** , na guia **Publicar** do Microsoft Office Backstage e editar a transformação no seu editor XML preferido, como o bloco de notas ou o Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="55216-108">To do so, extract the form into its component files by using **Export Source Files** on the **Publish** tab of the Microsoft Office Backstage, and then edit the transform in your preferred XML editor, such as Microsoft Visual Studio or Notepad.</span></span> 
  
<span data-ttu-id="55216-109">Se você fazer alterações em uma transformação de modo de exibição fora do InfoPath e, em seguida, abra a exibição no modo de design e fazer alterações, o InfoPath substituirá as alterações feitas manualmente.</span><span class="sxs-lookup"><span data-stu-id="55216-109">If you make changes to a view transform outside of InfoPath and then open the view in design mode and make changes, InfoPath will overwrite the changes you made manually.</span></span> <span data-ttu-id="55216-110">Para manter o InfoPath substituam as alterações feitas, coloque essas alterações em um `<xsl:template>` elemento na transformação e o uso do `xd:preserve` modo, conforme mostrado aqui:</span><span class="sxs-lookup"><span data-stu-id="55216-110">To keep InfoPath from overwriting the changes you make, you must place those changes in an  `<xsl:template>` element in the transform and use the  `xd:preserve` mode, as shown here:</span></span> 
  
```XML
<xsl:template match="my:field1" mode="xd:preserve"> 
   <div> 
      The value of field1 is <xsl:value-of select="."/> 
   </div> 
</xsl:template>
```

<span data-ttu-id="55216-111">Para incluir o modelo no arquivo transformado, use o `<xsl:apply-templates>` elemento com o mesmo `xd:preserve` modo:</span><span class="sxs-lookup"><span data-stu-id="55216-111">To include the template in the transformed file, use the  `<xsl:apply-templates>` element with the same  `xd:preserve` mode:</span></span> 
  
```XML
<xsl:apply-templates select="my:field1" mode="xd:preserve"/>
```

<span data-ttu-id="55216-112">Elementos e construções definidas dentro de modelos XSL com o `xd:preserve` modo não será exibido no ambiente de design do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="55216-112">Elements and constructs defined within XSL templates with the  `xd:preserve` mode will not be displayed in the InfoPath design environment.</span></span> <span data-ttu-id="55216-113">Em vez disso, o InfoPath marcará a seção personalizada com um controle rotulado **Preservar o bloco de código** com uma borda vermelha.</span><span class="sxs-lookup"><span data-stu-id="55216-113">Instead, InfoPath will mark the custom section with a control labeled **Preserve Code Block** with a red border.</span></span> <span data-ttu-id="55216-114">Quando um usuário abre o formulário para preenchê-lo, as transformações XSL personalizadas são aplicadas e os controles de **Preservar o bloco de código** não serão exibida.</span><span class="sxs-lookup"><span data-stu-id="55216-114">When a user opens the form to fill it out, the custom XSL transforms are applied and the **Preserve Code Block** controls will not appear.</span></span> 
  

