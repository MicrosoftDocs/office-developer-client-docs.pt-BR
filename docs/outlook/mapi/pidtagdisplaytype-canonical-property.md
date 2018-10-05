---
title: Propriedade canônica PidTagDisplayType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayType
api_type:
- HeaderDef
ms.assetid: ee2bc6ca-3769-4b56-a77d-81418d28f768
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: da26fd2a8643817cf60adbfa6f4e85da345b875c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393464"
---
# <a name="pidtagdisplaytype-canonical-property"></a>Propriedade canônica PidTagDisplayType

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um valor usado para associar um ícone com uma linha específica de uma tabela. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_DISPLAY_TYPE  <br/> |
|Identificador:  <br/> |0x3900  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Catálogo de endereços MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade contém um inteiro longo que facilita o tratamento especial de entrada da tabela com base em seu tipo. Este tratamento especial consiste tipicamente exibindo um ícone ou outro elemento de exibição, associado com o tipo de exibição. 
  
Essa propriedade não é usada nas tabelas de conteúdo de pasta. Aplicativos de cliente devem usar propriedade **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) e a interface de [IMAPIFormInfo](imapiforminfoimapiprop.md) apropriada de uma mensagem para obter o **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) e **PR_MINI_ICON** ([ PidTagMiniIcon](pidtagminiicon-canonical-property.md)) propriedades de mensagem. 
  
Essa propriedade pode ter exatamente um dos seguintes valores:
  
DT_AGENT 
  
> Um operador automatizado, como a citação do dia ou uma exibição de gráfico de clima.
    
DT_DISTLIST 
  
> Uma lista de distribuição.
    
DT_FOLDER 
  
> Exibe o ícone de pasta padrão adjacente à pasta.
    
DT_FOLDER_LINK 
  
> Exibe o ícone do link de pasta padrão adjacente à pasta em vez de um ícone de pasta padrão.
    
DT_FOLDER_SPECIAL 
  
> Exibe o ícone de uma pasta com uma distinção de aplicativo específico, como um tipo especial de pasta pública.
    
DT_FORUM 
  
> Um fórum, como um serviço do quadro de avisos ou uma pasta pública ou compartilhada.
    
DT_GLOBAL 
  
> Um catálogo de endereços global.
    
DT_LOCAL 
  
> Catálogo de endereços local que você compartilha com um pequeno grupo de trabalho.
    
DT_MAILUSER 
  
> Um usuário típico de mensagens.
    
DT_MODIFIABLE 
  
> Pode ser modificado; o contêiner deve ser indicado como modificável na interface do usuário.
    
DT_NOT_SPECIFIC 
  
> Não corresponde a qualquer uma das outras configurações.
    
DT_ORGANIZATION 
  
> Um alias especial definido para um grupo grande, como assistência técnica, contabilidade ou coordenador sangue-unidade.
    
DT_PRIVATE_DISTLIST 
  
> Uma privada, pessoalmente administrado a lista de distribuição.
    
DT_REMOTE_MAILUSER 
  
> Um destinatário sabidamente de um sistema de mensagens estrangeiro ou remoto.
    
DT_WAN 
  
> Um catálogo de endereços de rede de longa distância.
    
Tabelas de conteúdo de catálogo de endereços usam os valores DT_AGENT, DT_DISTLIST, DT_FORUM, DT_MAILUSER, DT_ORGANIZATION, DT_PRIVATE_DISTLIST e DT_REMOTE_MAILUSER. Tabelas de hierarquias de catálogo de endereços e tabelas únicas usam os valores DT_GLOBAL, DT_LOCAL, DT_MODIFIABLE, DT_NOT_SPECIFIC e DT_WAN. Tabelas de hierarquias de pasta usam os valores DT_FOLDER, DT_FOLDER_LINK e DT_FOLDER_SPECIAL. 
  
Se essa propriedade não estiver definida, o cliente deve presumir tipo padrão apropriado para a tabela, normalmente DT_FOLDER, DT_LOCAL ou DT_MAILUSER. 
  
 **Observação** Todos os valores não documentados são reservados para MAPI. Aplicativos cliente não devem definir qualquer novos valores e devem estar preparados para lidar com um valor não documentado. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Trata objetos de mensagem e o anexo.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas para modelos de catálogo de endereços.
    
[[MS-OXLDAP]](https://msdn.microsoft.com/library/727c090a-f05c-4eed-94aa-565724cfc550%28Office.15%29.aspx)
  
> Permite o acesso ao diretório.
    
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

