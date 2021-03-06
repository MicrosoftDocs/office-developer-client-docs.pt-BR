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
ms.openlocfilehash: fc2774efed1a15fe79e167149f2cb162bae7642c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358531"
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

O cliente de email e o servidor devem gerar uma mensagem de resolução de conflito ao detectar um conflito com a versão atual de uma mensagem na réplica durante a sincronização. É importante entender que é possível que a versão atual da mensagem na réplica local seja transmitida durante a operação de sincronização atual. Isso acontecerá quando o conflito já existir no servidor antes que qualquer uma das mensagens conflitantes seja baixada para a réplica local. Uma mensagem de resolução de conflito deve ser sincronizada como réplicas independentes com PCLs conflitantes. A mensagem de resolução de conflito em si não deve ser sincronizada entre o cliente e o servidor; somente as réplicas independentes devem ser trocadas. O parceiro de sincronização deve gerar uma nova mensagem que corresponde à estrutura da mensagem de conflito. Portanto, é importante que o cliente e o servidor usem o mesmo algoritmo para detectar o item "vencedor". As regras a seguir devem ser aplicadas para detectar o "vencedor":
  
1. Hora da última modificação.
    
2. GUID cn superior (usando a comparação de memória) para quebrar o vínculo.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Lida com a sincronização de dados de objeto de mensagens entre um servidor e um cliente.
    
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

