---
title: Usando XSLT personalizado em modelos de formulário do InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 32c80bcd-a5d6-af32-38ba-9ca9ff148b99
description: Você pode criar a maioria dos elementos de exibição que provavelmente precisará no designer de formulário do Microsoft InfoPath. No entanto, se você precisar de um elemento de modo de exibição personalizado que o InfoPath não possa criar para você, poderá modificar manualmente a XSL Transformation (XSLT) que o InfoPath usa para gerar o modo de exibição. Para fazer isso, extraia o formulário em seus arquivos de componente usando Exportar Arquivos de Origem na guia Publicar do Microsoft Office Backstage e edite a transformação em seu editor XML preferido, como o Microsoft Visual Studio ou o Bloco de Notas.
ms.openlocfilehash: a61980191dbedeec33b06ad8173ce50126fea781
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428267"
---
# <a name="using-custom-xslt-in-infopath-form-templates"></a>Usando XSLT personalizado em modelos de formulário do InfoPath

Você pode criar a maioria dos elementos de exibição que provavelmente precisará no designer de formulário do Microsoft InfoPath. No entanto, se você precisar de um elemento de modo de exibição personalizado que o InfoPath não possa criar para você, poderá modificar manualmente a XSL Transformation (XSLT) que o InfoPath usa para gerar o modo de exibição. Para fazer isso, extraia o formulário  em seus  arquivos de componente usando Exportar Arquivos de Origem na guia Publicar do Microsoft Office Backstage e edite a transformação em seu editor XML preferido, como o Microsoft Visual Studio ou o Bloco de Notas. 
  
Se você fizer alterações em uma transformação de exibição fora do InfoPath e, em seguida, abrir o modo de exibição no modo de design e fazer alterações, o InfoPath substituirá as alterações feitas manualmente. Para impedir que o InfoPath sobrescreva as alterações feitas, você deve colocar essas alterações em um elemento na transformação e usar o  `<xsl:template>`  `xd:preserve` modo, conforme mostrado aqui: 
  
```XML
<xsl:template match="my:field1" mode="xd:preserve"> 
   <div> 
      The value of field1 is <xsl:value-of select="."/> 
   </div> 
</xsl:template>
```

Para incluir o modelo no arquivo transformado, use  `<xsl:apply-templates>` o elemento com o mesmo  `xd:preserve` modo: 
  
```XML
<xsl:apply-templates select="my:field1" mode="xd:preserve"/>
```

Elementos e construções definidos em modelos XSL com o modo não  `xd:preserve` serão exibidos no ambiente de design do InfoPath. Em vez disso, o InfoPath marcará a seção personalizada com um controle rotulado como Preservar Bloco de **Código** com uma borda vermelha. Quando um usuário abre o formulário para preenchê-lo, as transformação  XSL personalizadas são aplicadas e os controles preservar bloco de código não serão exibidos. 
  

