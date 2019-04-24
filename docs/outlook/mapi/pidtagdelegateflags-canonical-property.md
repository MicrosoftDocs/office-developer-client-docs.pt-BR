---
title: Propriedade canônica PidTagDelegateFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDelegateFlags
api_type:
- HeaderDef
ms.assetid: 3a504594-204c-472c-8be7-dca154c94ea2
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 20ffc6f7f4d21f980e5f0f387464430ba187192a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359896"
---
# <a name="pidtagdelegateflags-canonical-property"></a>Propriedade canônica PidTagDelegateFlags

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica se um representante pode exibir os objetos de mensagem privada do delegante.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_DELEGATE_FLAGS  <br/> |
|Identificador:  <br/> |0x686B  <br/> |
|Tipo de dados:  <br/> |PT_MV_LONG  <br/> |
|Área:  <br/> |Transmissão definida pela classe da mensagem-transmittable  <br/> |
   
## <a name="remarks"></a>Comentários

Cada entrada dessa propriedade deve ser definida como um dos valores a seguir.
  
|**Flag**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|HidePrivate  <br/> |,0  <br/> |O representante não deve ter permissão para exibir objetos de mensagem privados.  <br/> |
|Pessoal  <br/> |1  <br/> |O representante deve ter permissão para exibir objetos de mensagem privados.  <br/> |
   
Essa propriedade deve ser definida no objeto delegate Information. O valor de "tudo privado" indica que o delegante deseja tornar os objetos de mensagens particulares visíveis. Essa preferência é aplicável a todas as pastas para as quais o representante tem uma função de revisor, autor ou editor.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Especifica métodos para conectar e configurar caixas de correio como delegados e interações com objetos de mensagem e calendário quando eles atuam em nome de outro usuário.
    
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

