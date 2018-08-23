---
title: Propriedade canônica PidTagInConflict
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInConflict
api_type:
- HeaderDef
ms.assetid: e83c05c6-a7c0-486c-a112-58a39255767a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 33bf77029207e2d8d734d5c49735262135896660
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593722"
---
# <a name="pidtaginconflict-canonical-property"></a>Propriedade canônica PidTagInConflict

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém TRUE quando o anexo representa uma réplica alternativa.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_IN_CONFLICT  <br/> |
|Identificador:  <br/> |0x666C  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Observação de conflito  <br/> |
   
## <a name="remarks"></a>Comentários

O cliente de email e o servidor devem gerar uma mensagem de resolução de conflito quando detectar um conflito contra a versão atual de uma mensagem na réplica durante a sincronização. É importante entender o que é possível que a versão atual da mensagem na réplica local foi transmitida durante a operação de sincronização atual. Isso acontecerá quando o conflito já existe no servidor antes de qualquer uma das mensagens conflitantes foram baixados para a réplica local. Um conflito resolver mensagem deve ser sincronizada como independentes réplicas com PCLs conflitantes. O conflito resolver mensagem propriamente dita não deve ser sincronizada entre cliente e servidor; somente as réplicas independentes que devem ser trocadas. O parceiro de sincronização deve gerar uma nova mensagem que corresponda à estrutura da mensagem de conflito. Portanto, é importante que o cliente e servidor usam o mesmo algoritmo para detectar o item "prêmio". As regras a seguir devem ser aplicadas para detectar o "prêmio":
  
1. Hora da última modificação.
    
2. Superior CN GUID (usando a comparação de memória) para quebrar tie.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Trata-se de sincronização de dados de objeto de mensagens entre um servidor e um cliente.
    
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

