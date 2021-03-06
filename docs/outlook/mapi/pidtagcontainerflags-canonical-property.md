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
ms.openlocfilehash: c9c446097213e5b743a47ec32db17ec0afe63b78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357544"
---
# <a name="pidtagcontainerflags-canonical-property"></a>Propriedade canônica PidTagContainerFlags

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma máscara de bits de sinalizadores que descrevem as funcionalidades de um contêiner de um livro de endereços. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_CONTAINER_FLAGS  <br/> |
|Identificador:  <br/> |0x3600  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Catálogo de endereços  <br/> |
   
## <a name="remarks"></a>Comentários

Um ou mais dos sinalizadores a seguir podem ser definidos para a máscara de bits:
  
AB_FIND_ON_OPEN 
  
> Exibe uma caixa de diálogo para solicitar uma restrição antes de exibir qualquer conteúdo do contêiner. 
    
AB_MODIFIABLE 
  
> As entradas podem ser adicionadas e removidas do contêiner. Esse sinalizador não indica se alguma entrada no contêiner pode ser modificada.
    
AB_RECIPIENTS 
  
> O contêiner pode conter destinatários. Esse sinalizador não indica se algum destinatário está realmente presente no contêiner ou se eles podem ser adicionados ou removidos. 
    
AB_SUBCONTAINERS 
  
> O contêiner pode conter contêineres filho. Esse sinalizador não indica se quaisquer subcontainers estão realmente presentes no contêiner, nem se eles podem ser adicionados ou removidos. AB_SUBCONTAINERS deve ser definido para que o contêiner suporte [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md). 
    
AB_UNMODIFIABLE 
  
> As entradas não podem ser adicionadas ou removidas do contêiner. Esse sinalizador não indica se alguma entrada no contêiner pode ser modificada. 
    
O AB_FIND_ON_OPEN é altamente recomendado para contêineres usados com serviços online ou com conexões lentas com servidores. Quando um contêiner é aberto com AB_FIND_ON_OPEN  definido, uma caixa de diálogo Encontrar é apresentada ao usuário para restringir os usuários de mensagens exibidos. Até mesmo uma especificação parcial limitando os usuários de mensagens pode acelerar drasticamente a exibição do conteúdo. 
  
O sinalizador AB_MODIFIABLE ou AB_UNMODIFIABLE deve ser definido. Ambos os sinalizadores podem ser definidos para indicar que o contêiner não sabe se pode ser modificado ou não, por exemplo, se a modificação depende dos direitos de acesso do usuário. Nesse caso, um aplicativo cliente deve tentar uma chamada e examinar o código de retorno para determinar os recursos do contêiner. Um cliente normalmente começa examinando AB_MODIFIABLE. Se estiver definido, o cliente faz uma chamada que tenta modificar o contêiner e verifica o valor de retorno. 
  
O AB_MODIFIABLE sinalizador não indica quais tipos de entradas podem ser adicionadas ao contêiner. Para determinar isso, o cliente deve usar o método [OpenProperty](imapiprop-openproperty.md) apropriado para abrir a propriedade **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) do contêiner. Abrir **PR_CREATE_TEMPLATES** faz com que a tabela única do contêiner seja retornada, listando os tipos de entradas que podem ser criadas no contêiner. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para listas de usuários, contatos, grupos e recursos.
    
[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)
  
> Lida com as comunicações de um cliente com um servidor NSPI (Name Service Provider Interface).
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

