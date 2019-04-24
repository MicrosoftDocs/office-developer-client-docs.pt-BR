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
ms.openlocfilehash: 834141fe3e57fde5e6404776e0ad5ce3b438450e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360799"
---
# <a name="pidtagdisplayname-canonical-property"></a>Propriedade canônica PidTagDisplayName

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o nome para exibição de um determinado objeto MAPI. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_DISPLAY_NAME, PR_DISPLAY_NAME_A, PR_DISPLAY_NAME_W  <br/> |
|Identificador:  <br/> |0x3001  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |MAPI comum  <br/> |
   
## <a name="remarks"></a>Comentários

As pastas exigem subpastas irmãs para ter nomes de exibição exclusivos. Por exemplo, se uma pasta contiver duas subpastas, as duas subpastas não poderão usar o mesmo valor para essa propriedade. Essa restrição não se aplica a outros contêineres, como catálogos de endereços e listas de distribuição. 
  
Os provedores de serviços devem definir o valor dessa propriedade para que contenham o tipo de provedor e informações de configuração. As informações adicionais ajudam a distinguir entre instâncias de provedores do mesmo tipo. Provedores não configurados devem usar uma cadeia de caracteres que nomeia o provedor. Os provedores conFigurados devem usar a mesma cadeia de caracteres seguida de uma cadeia de caracteres de distinção entre parênteses. Por exemplo, um provedor de repositório de mensagens não configurado pode definir essas propriedades como: 
  
Repositório de informações pessoais
  
A versão configurada pode então definir essas propriedades como: 
  
Repositório de informações pessoais (6 de fevereiro de 1998)
  
Para objetos status, essas propriedades contêm o nome do componente que pode ser exibido pela interface do usuário. 
  
> [!NOTE]
> Pontos-e-vírgulas não podem ser usados em nomes de destinatários em mensagens MAPI. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Manipula objetos Message e Attachment.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Controla as operações da pasta.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica as propriedades e as operações que são permitidas para contatos e listas de distribuição pessoal.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica as propriedades e operações de listas de usuários, contatos, grupos e recursos.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Converte as convenções de email padrão da Internet em objetos de mensagem.
    
[[MS-XWDVSEC]](https://msdn.microsoft.com/library/dc043d09-6b76-4392-aea3-68f8e81c64d8%28Office.15%29.aspx)
  
> Estende o protocolo WebDAV que especifica como solicitar e definir o descritor de segurança do Exchange por meio de métodos WebDAV.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

