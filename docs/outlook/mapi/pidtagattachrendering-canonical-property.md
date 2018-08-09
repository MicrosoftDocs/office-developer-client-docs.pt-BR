---
title: Propriedade canônica PidTagAttachRendering
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachRendering
api_type:
- HeaderDef
ms.assetid: 1f31f7f4-fbda-4337-95e5-5474dd1bf84a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a1df3ba8e57f1e91894b88d7e8a72feb681e13dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768985"
---
# <a name="pidtagattachrendering-canonical-property"></a>Propriedade canônica PidTagAttachRendering

  
  
**Aplica-se a**: Outlook 
  
Contém um metarquivo do Microsoft Windows com informações de renderização de um anexo. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ATTACH_RENDERING  <br/> |
|Identificador:  <br/> |0x3709  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Anexo de mensagem  <br/> |
   
## <a name="remarks"></a>Comentários

A finalidade dessa propriedade é fornecer um ícone ou outra representação visual que pode ser exibida dentro da mensagem pai no ponto de anexo. Tal representação normalmente inclui o nome do anexo, se houver e a natureza do anexo, como um documento do Microsoft Office Word. Um aplicativo cliente pode usar esta representação na exibição da mensagem. 
  
Para um arquivo anexado, essa propriedade normalmente retrata um ícone para o arquivo. 
  
Para uma mensagem anexada, essa propriedade normalmente não estiver definida. Um aplicativo cliente que precisam renderizar uma mensagem anexada deve obter sua propriedade **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), chame [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) para um ponteiro para o objeto de informações de formulário correspondente, Abra a interface [IMAPIFormInfo](imapiforminfoimapiprop.md) em tal objeto e use **GetProps** para recuperar o **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) ou a propriedade **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)). 
  
Para um objeto OLE estático incorporado, essa propriedade contém um metarquivo do Microsoft Windows que pode ser usado para desenhar a representação de anexo em uma janela. 
  
Para um objeto OLE dinâmico incorporado, o cliente deve usar os dados OLE para gerar as informações de renderização. 
  
Em todos os casos, o aplicativo cliente deve estar ciente que essa propriedade normalmente é centenas de bytes em tamanho e está sujeito às truncamento na tabela de anexo. Se um cliente quiser renderizar o anexo a partir dessa propriedade sem abrir o anexo em si, ele deve trabalhar dentro da regra de truncamento de tabela. Para obter mais informações, consulte [Trabalhando com grandes colunas](working-with-large-columns.md). 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Trata objetos de mensagem e o anexo.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

