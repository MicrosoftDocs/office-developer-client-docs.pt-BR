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
ms.openlocfilehash: 22d3e649641dbe688912ecece7fde73a555f4a88
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361093"
---
# <a name="pidtagattachrendering-canonical-property"></a>Propriedade canônica PidTagAttachRendering

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um metarquivo do Microsoft Windows com informações de renderização de um anexo. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ATTACH_RENDERING  <br/> |
|Identificador:  <br/> |0x3709  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Anexo de mensagem  <br/> |
   
## <a name="remarks"></a>Comentários

A finalidade dessa propriedade é fornecer um ícone ou outra representação de ilustrações que possa ser exibida dentro da mensagem pai no ponto de anexo. Essa representação normalmente inclui o nome do anexo, se houver, e a natureza do anexo, como um documento do Microsoft Office Word. Um aplicativo cliente pode usar essa representação na exibição da mensagem. 
  
Para um arquivo anexado, essa propriedade normalmente retrata um ícone para o arquivo. 
  
Para uma mensagem anexada, esta propriedade normalmente não é definida. Um aplicativo cliente que precisa processar uma mensagem anexada deve obter sua propriedade **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), chamar [IMAPIFormMgr:: ResolveMessageClass](imapiformmgr-resolvemessageclass.md) para um ponteiro para o objeto de informações de formulário correspondente Abra a interface [IMAPIFormInfo](imapiforminfoimapiprop.md) nesse objeto e use GetProps para recuperar a propriedade **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) ou **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)). **** 
  
Para um objeto OLE estático incorporado, esta propriedade contém um metarquivo do Microsoft Windows que pode ser usado para desenhar a representação de anexo em uma janela. 
  
Para um objeto OLE dinâmico incorporado, o cliente deve usar os dados OLE para gerar as informações de renderização. 
  
Em todos os casos, o aplicativo cliente deve estar ciente de que essa propriedade normalmente é de várias centenas de bytes de tamanho e está sujeita a truncamento na tabela de anexos. Se um cliente quiser renderizar o anexo dessa propriedade sem abrir o próprio anexo, ele deverá funcionar dentro da regra de truncamento da tabela. Para obter mais informações, consulte [trabalhar com colunas grandes](working-with-large-columns.md). 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Manipula objetos Message e Attachment.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

