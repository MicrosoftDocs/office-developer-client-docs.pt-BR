---
title: Propriedade canônica PidLidAppointmentAuxiliaryFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentAuxiliaryFlags
api_type:
- COM
ms.assetid: 56c64e23-4a99-4f80-ba06-dfae2a5fe961
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: cac9c735403e6cb65dfe3111a2246a8387339339
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768207"
---
# <a name="pidlidappointmentauxiliaryflags-canonical-property"></a>Propriedade canônica PidLidAppointmentAuxiliaryFlags

  
  
**Aplica-se a**: Outlook 
  
Especifica um campo de bit que descreve o estado auxiliar do objeto.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidApptAuxFlags  <br/> |
|Propriedade definida:  <br/> |PSETID_Appointment  <br/> |
|ID de longo (LID):  <br/> |0x00008207  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Reuniões  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade não é necessária. Abaixo estão os sinalizadores individuais que podem ser definidos.
  
C (auxApptFlagCopied 0x00000001)
  
> Esse sinalizador indica que o objeto calendar foi copiado de outra pasta de calendário.
    
R (auxApptFlagForceMtgResponse, 0x00000002)
  
> Esse sinalizador em uma solicitação de reunião indica que o cliente ou servidor deve enviar uma resposta de reunião ao organizador quando uma resposta é escolhida.
    
F (auxApptFlagForwarded 0x00000004)
  
> Esse sinalizador em uma solicitação de reunião indica que ele foi encaminhado (incluindo sejam encaminhadas pelo organizador), em vez de ser um convite do organizador.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

