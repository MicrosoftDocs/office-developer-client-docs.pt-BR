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
ms.openlocfilehash: 4414ae866dece0654131d1575fe699676892709f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345427"
---
# <a name="pidlidappointmentauxiliaryflags-canonical-property"></a>Propriedade canônica PidLidAppointmentAuxiliaryFlags

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica um campo de bits que descreve o estado auxiliar do objeto.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidApptAuxFlags  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Appointment  <br/> |
|Long ID (LID):  <br/> |0x00008207  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Meetings  <br/> |
   
## <a name="remarks"></a>Comentários

Esta propriedade não é obrigatória. Veja a seguir os sinalizadores individuais que podem ser definidos.
  
C (auxApptFlagCopied, 0x00000001)
  
> Este sinalizador indica que o objeto Calendar foi copiado de outra pasta de calendário.
    
R (auxApptFlagForceMtgResponse, 0x00000002)
  
> Esse sinalizador em uma solicitação de reunião indica que o cliente ou servidor deve enviar uma resposta de reunião de volta para o organizador quando uma resposta for escolhida.
    
F (auxApptFlagForwarded, 0x00000004)
  
> Esse sinalizador em uma solicitação de reunião indica que ela foi encaminhada (incluindo ser encaminhada pelo organizador), em vez de ser um convite do organizador.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica as propriedades e as operações de compromisso, solicitação de reunião e mensagens de resposta.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

