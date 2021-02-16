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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360778"
---
# <a name="pidtagdisplaytype-canonical-property"></a>Propriedade canônica PidTagDisplayType

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um valor usado para associar um ícone a uma linha específica de uma tabela. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_DISPLAY_TYPE  <br/> |
|Identificador:  <br/> |0x3900  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |MapI address book  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade contém um inteiro longo que facilita o tratamento especial da entrada da tabela com base em seu tipo. Esse tratamento especial geralmente consiste em exibir um ícone ou outro elemento de exibição associado ao tipo de exibição. 
  
Essa propriedade não é usada em tabelas de conteúdo de pastas. Os aplicativos cliente devem usar a propriedade **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) de uma mensagem e a interface [IMAPIFormInfo](imapiforminfoimapiprop.md) apropriada para obter as propriedades **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) e **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) para essa mensagem. 
  
Essa propriedade pode ter exatamente um dos seguintes valores:
  
DT_AGENT 
  
> Um agente automatizado, como Quote-of-The-Day ou uma exibição de gráfico de previsão do tempo.
    
DT_DISTLIST 
  
> Uma lista de distribuição.
    
DT_FOLDER 
  
> Exibe o ícone de pasta padrão adjacente à pasta.
    
DT_FOLDER_LINK 
  
> Exibe o ícone de link de pasta padrão adjacente à pasta em vez do ícone de pasta padrão.
    
DT_FOLDER_SPECIAL 
  
> Ícone de exibição para uma pasta com uma distinção específica do aplicativo, como um tipo especial de pasta pública.
    
DT_FORUM 
  
> Um fórum, como um serviço de quadro de boletins ou uma pasta pública ou compartilhada.
    
DT_GLOBAL 
  
> Um livro de endereços global.
    
DT_LOCAL 
  
> Um livro de endereços local que você compartilha com um pequeno grupo de trabalho.
    
DT_MAILUSER 
  
> Um usuário de mensagens típico.
    
DT_MODIFIABLE 
  
> Modificável; o contêiner deve ser denodado como modificável na interface do usuário.
    
DT_NOT_SPECIFIC 
  
> Não é igual a nenhuma das outras configurações.
    
DT_ORGANIZATION 
  
> Um alias especial definido para um grupo grande, como helpdesk, accounting ou coordenador de unidade de sol.
    
DT_PRIVATE_DISTLIST 
  
> Uma lista de distribuição privada e administrada pessoalmente.
    
DT_REMOTE_MAILUSER 
  
> Um destinatário conhecido por ser de um sistema de mensagens externo ou remoto.
    
DT_WAN 
  
> Um livro de endereços de rede de área ampla.
    
As tabelas de conteúdo do livro de endereços usam os valores DT_AGENT, DT_DISTLIST, DT_FORUM, DT_MAILUSER, DT_ORGANIZATION, DT_PRIVATE_DISTLIST e DT_REMOTE_MAILUSER. As tabelas de hierarquia do livro de endereços e as tabelas one-off usam os valores DT_GLOBAL, DT_LOCAL, DT_MODIFIABLE, DT_NOT_SPECIFIC e DT_WAN dados. As tabelas de hierarquia de pastas usam DT_FOLDER, DT_FOLDER_LINK e DT_FOLDER_SPECIAL pasta. 
  
Se essa propriedade não estiver definida, o cliente deverá assumir o tipo padrão apropriado para a tabela, normalmente DT_FOLDER, DT_LOCAL ou DT_MAILUSER. 
  
 **Observação** Todos os valores não documentados são reservados para MAPI. Os aplicativos cliente não devem definir novos valores e devem estar preparados para lidar com um valor não documentado. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Lida com objetos de mensagem e anexo.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas para modelos de livro de endereços.
    
[[MS-OXLDAP]](https://msdn.microsoft.com/library/727c090a-f05c-4eed-94aa-565724cfc550%28Office.15%29.aspx)
  
> Habilita o acesso ao diretório.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

