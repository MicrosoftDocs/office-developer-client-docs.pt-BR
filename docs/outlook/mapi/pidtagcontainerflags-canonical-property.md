---
title: Propriedade canônica PidTagContainerFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerFlags
api_type:
- HeaderDef
ms.assetid: 66b8d333-227e-464d-8cf9-cd8a5ff15efb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c13acd1c3b759602a5fbe07c21ca8b784e0fe4d1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769084"
---
# <a name="pidtagcontainerflags-canonical-property"></a>Propriedade canônica PidTagContainerFlags

  
  
**Aplica-se a**: Outlook 
  
Contém uma bitmask dos sinalizadores que descrevem os recursos de um contêiner de catálogo de endereços. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_CONTAINER_FLAGS  <br/> |
|Identificador:  <br/> |0x3600  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Catálogo de endereços  <br/> |
   
## <a name="remarks"></a>Comentários

Um ou mais dos seguintes sinalizadores podem ser definido para a máscara de bits:
  
AB_FIND_ON_OPEN 
  
> Exibe uma caixa de diálogo para solicitar uma restrição antes de exibir qualquer conteúdo do contêiner. 
    
AB_MODIFIABLE 
  
> Entradas podem ser adicionadas ao e removidas do contêiner. Esse sinalizador não indica se as entradas no contêiner podem ser modificadas.
    
AB_RECIPIENTS 
  
> O contêiner pode manter os destinatários. Esse sinalizador não indica se quaisquer destinatários estão realmente presentes no contêiner ou se eles podem ser adicionados ou removidos. 
    
AB_SUBCONTAINERS 
  
> O contêiner pode manter filho contêineres. Esse sinalizador não indica se qualquer subcontêineres são realmente presentes no contêiner, nem se eles podem ser adicionados ou removidos. AB_SUBCONTAINERS deve ser definida para o contêiner oferecer suporte a [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md). 
    
AB_UNMODIFIABLE 
  
> As entradas não podem ser adicionadas ou removidas do contêiner. Esse sinalizador não indica se as entradas no contêiner podem ser modificadas. 
    
O sinalizador AB_FIND_ON_OPEN é altamente recomendável para contêineres usados com os serviços online ou com conexões lentas aos servidores. Quando for aberto um contêiner que tenha AB_FIND_ON_OPEN definida, uma caixa de diálogo **Localizar** é apresentada ao usuário para restringir os usuários de mensagens exibidos. Mesmo uma especificação parcial limitando os usuários de mensagens pode acelerar drasticamente uma exibição do conteúdo. 
  
Sinalizador a AB_MODIFIABLE ou AB_UNMODIFIABLE deve ser definida. Ambos os sinalizadores podem ser definidos para indicar que o contêiner não sabe se ele pode ser modificado ou não, por exemplo, se a modificação depende de direitos de acesso do usuário. Nesse caso, um aplicativo cliente deve executar uma tentativa de uma chamada e examinar o código de retorno para determinar os recursos do contêiner. Geralmente, um cliente inicia examinando AB_MODIFIABLE. Se ele estiver definido, o cliente faz uma chamada que tenta modificar o contêiner e verifica se o valor de retorno. 
  
O sinalizador AB_MODIFIABLE não indica quais tipos de entradas podem ser adicionados ao contêiner. Para determinar isso, o cliente deve usar o método [OpenProperty](imapiprop-openproperty.md) apropriado para abrir a propriedade de **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) do contêiner. Abertura **PR_CREATE_TEMPLATES** causas one-off do contêiner de tabela para serem retornadas, listando os tipos de entradas que podem ser criados no contêiner. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para obter listas de usuários, contatos, grupos e recursos.
    
[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)
  
> Trata a comunicação do cliente com um servidor de nome serviço provedor NSPI (Interface).
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

