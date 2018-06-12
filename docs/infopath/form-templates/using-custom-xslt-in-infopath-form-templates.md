---
title: Usando o XSLT personalizado em modelos de formulário do InfoPath
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
# <a name="using-custom-xslt-in-infopath-form-templates"></a>Usando o XSLT personalizado em modelos de formulário do InfoPath

Você pode criar a maioria dos elementos de modo de exibição, que você provavelmente precisa no Microsoft InfoPath form designer. Se você precisar de um elemento de exibição personalizada que InfoPath não pode criar para você, no entanto, você pode modificar manualmente o XSL Transformation (XSLT) que usa o InfoPath para gerar o modo de exibição. Para fazer isso, extrair o formulário em seus arquivos de componente usando **Exportar arquivos de origem** , na guia **Publicar** do Microsoft Office Backstage e editar a transformação no seu editor XML preferido, como o bloco de notas ou o Microsoft Visual Studio. 
  
Se você fazer alterações em uma transformação de modo de exibição fora do InfoPath e, em seguida, abra a exibição no modo de design e fazer alterações, o InfoPath substituirá as alterações feitas manualmente. Para manter o InfoPath substituam as alterações feitas, coloque essas alterações em um `<xsl:template>` elemento na transformação e o uso do `xd:preserve` modo, conforme mostrado aqui: 
  
```XML
<xsl:template match="my:field1" mode="xd:preserve"> 
   <div> 
      The value of field1 is <xsl:value-of select="."/> 
   </div> 
</xsl:template>
```

Para incluir o modelo no arquivo transformado, use o `<xsl:apply-templates>` elemento com o mesmo `xd:preserve` modo: 
  
```XML
<xsl:apply-templates select="my:field1" mode="xd:preserve"/>
```

Elementos e construções definidas dentro de modelos XSL com o `xd:preserve` modo não será exibido no ambiente de design do InfoPath. Em vez disso, o InfoPath marcará a seção personalizada com um controle rotulado **Preservar o bloco de código** com uma borda vermelha. Quando um usuário abre o formulário para preenchê-lo, as transformações XSL personalizadas são aplicadas e os controles de **Preservar o bloco de código** não serão exibida. 
  

