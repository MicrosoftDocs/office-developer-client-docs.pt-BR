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
# <a name="using-custom-xslt-in-infopath-form-templates"></a>Usando XSLT personalizado em modelos de formulário do InfoPath

Você pode criar a maior parte dos elementos de exibição que provavelmente precisará no designer de formulários do Microsoft InfoPath. No entanto, se você precisar de um elemento de exibição personalizado que o InfoPath não possa criar para você, poderá modificar manualmente a transformação em XSL (XSLT) que o InfoPath usa para gerar o modo de exibição. Para fazer isso, extraia o formulário em seus arquivos de componente usando **exportar arquivos de origem** na guia **publicar** do Microsoft Office Backstage e edite a transformação no editor de XML preferencial, como Microsoft Visual Studio ou bloco de notas. 
  
Se você fizer alterações em uma transformação de exibição fora do InfoPath e, em seguida, abrir o modo de exibição no modo de design e fizer alterações, o InfoPath substituirá as alterações feitas manualmente. Para impedir que o InfoPath substitua as alterações feitas, você deve colocar essas alterações em um `<xsl:template>` elemento na transformação e usar o `xd:preserve` modo, conforme mostrado aqui: 
  
```XML
<xsl:template match="my:field1" mode="xd:preserve"> 
   <div> 
      The value of field1 is <xsl:value-of select="."/> 
   </div> 
</xsl:template>
```

Para incluir o modelo no arquivo transformado, use `<xsl:apply-templates>` o elemento com o `xd:preserve` mesmo modo: 
  
```XML
<xsl:apply-templates select="my:field1" mode="xd:preserve"/>
```

Elementos e construções definidos em modelos XSL com o `xd:preserve` modo não serão exibidos no ambiente de design do InfoPath. Em vez disso, o InfoPath marcará a seção personalizada com um controle rotulado como **preservar bloco de código** com uma borda vermelha. Quando um usuário abre o formulário para preenchê-lo, as transformações XSL personalizadas são aplicadas e os controles de **preservar bloco de código** não serão exibidos. 
  

