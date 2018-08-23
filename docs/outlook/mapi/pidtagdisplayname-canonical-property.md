---
title: Propriedade canônica PidTagDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayName
api_type:
- HeaderDef
ms.assetid: bd094e00-5c60-4bb3-9a45-b943fab52876
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 70b0508d9a19df42e4ab164aba58aaef44b0c01a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565484"
---
# <a name="pidtagdisplayname-canonical-property"></a>Propriedade canônica PidTagDisplayName

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o nome de exibição para um determinado objeto MAPI. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_DISPLAY_NAME, PR_DISPLAY_NAME_A, PR_DISPLAY_NAME_W  <br/> |
|Identificador:  <br/> |0x3001  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |MAPI comuns  <br/> |
   
## <a name="remarks"></a>Comentários

As pastas requerem subpastas irmão tenham nomes para exibição exclusivos. Por exemplo, se uma pasta contém duas subpastas, as duas subpastas não podem usar o mesmo valor para essa propriedade. Essa restrição não se aplica a outros contêineres, como catálogos de endereços e listas de distribuição. 
  
Provedores de serviços devem definir o valor dessa propriedade para que ela contenha ambas as informações de configuração e o tipo de provedor. As informações adicionais ajudam a diferenciar instâncias dos provedores do mesmo tipo. Não configurados provedores devem usar uma cadeia de caracteres que nomeia o provedor. Provedores configurados devem usar a mesma cadeia seguida por uma cadeia de caracteres distintas entre parênteses. Por exemplo, um provedor de armazenamento de mensagem não configurado pode definir essas propriedades: 
  
Armazenamento de informações pessoais
  
A versão configurada, em seguida, pode definir essas propriedades: 
  
Armazenamento de informações pessoais (6 de fevereiro de 1998)
  
Para objetos de status, essas propriedades contêm o nome do componente que pode ser exibido pela interface do usuário. 
  
> [!NOTE]
> Ponto e vírgula não pode ser usada em nomes de destinatário em mensagens de MAPI. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Trata objetos de mensagem e o anexo.
    
[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Trata as operações de pasta.
    
[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas para contatos e listas de distribuição pessoal.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para obter listas de usuários, contatos, grupos e recursos.
    
[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Converte de convenções de email padrão da Internet para os objetos de mensagem.
    
[[MS-XWDVSEC]](http://msdn.microsoft.com/library/dc043d09-6b76-4392-aea3-68f8e81c64d8%28Office.15%29.aspx)
  
> Estende o protocolo WebDAV que especifica como solicitar e definir o descritor de segurança do Exchange por meio de métodos de WebDAV.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

