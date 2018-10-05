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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392274"
---
# <a name="pidtagdelegateflags-canonical-property"></a>Propriedade canônica PidTagDelegateFlags

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica se um representante pode exibir objetos de mensagem privada do representante.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_DELEGATE_FLAGS  <br/> |
|Identificador:  <br/> |0x686B  <br/> |
|Tipo de dados:  <br/> |PT_MV_LONG  <br/> |
|Área:  <br/> |Mensagem definida de classe transmittable  <br/> |
   
## <a name="remarks"></a>Comentários

Cada entrada dessa propriedade deve ser definida como um dos valores a seguir.
  
|**Flag**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|HidePrivate  <br/> |0  <br/> |O representante não deve ser permitido para exibir objetos de mensagem privada.  <br/> |
|ShowPrivate  <br/> |1  <br/> |O delegado deve ter permissão para exibir objetos de mensagem privada.  <br/> |
   
Essa propriedade deverá ser definida no objeto de informações do representante. O valor de "ShowPrivate" indica que o representante deseje tornar visíveis a objetos de mensagem privada. Esta preferência é aplicável a todas as pastas para o qual o representante tem uma função do revisor, autor ou editor.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Especifica os métodos para conexão e a configuração de caixas de correio conforme representantes e as interações com objetos de mensagem e o calendário quando eles ajam em nome de outro usuário.
    
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

