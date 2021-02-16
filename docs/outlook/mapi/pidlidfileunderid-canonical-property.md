---
title: Propriedade canônica PidLidFileUnderId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFileUnderId
api_type:
- COM
ms.assetid: 917431a9-fd90-4b4d-b042-886e3dbf47c0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7af30866a5fd2846327223b7a58c6de91f5fef7a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355703"
---
# <a name="pidlidfileunderid-canonical-property"></a>Propriedade canônica PidLidFileUnderId

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica como gerar e recomputar o valor da propriedade **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) quando outras propriedades de nome de contato mudarem.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidFileUnderId  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Address  <br/> |
|Long ID (LID):  <br/> |0x00008006  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Contato  <br/> |
   
## <a name="remarks"></a>Comentários

Se essa propriedade estiver ausente ou definida com um valor não detalhado na tabela abaixo ou em [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx), o aplicativo poderá escolher sua própria lógica para recomputar o valor de **dispidFileUnder** à medida que outras propriedades de nome de contato mudarem. 
  
Na tabela a seguir, a notação <PropertyName> é usada para especificar "o valor de PropertyName". Por exemplo, se o valor da propriedade **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md)) for "Smith" e o valor da propriedade **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) for "Ben", então " especificará a cadeia de <PidTagGivenName> <PidTagSurname> caracteres "Ben Smith". Na tabela, "\r" especifica um caractere de retorno de carro, "\n" especifica um caractere de alimentação de linha e representa <space> um caractere de espaço.
  
|**Valor da **propriedade dispidFileUnderId****|**Descrição da **propriedade dispidFileUnder****|
|:-----|:-----|
|0x00000000  <br/> |Vazio PT_UNICODE.  <br/> |
|0x00003001  <br/> |" \< PidTagDisplayName \> "  <br/> |
|0x00003A06  <br/> |" \< PidTagGivenName \> "  <br/> |
|0x00003A11  <br/> |" \< PidTagSurname \> "  <br/> |
|0x00003A16  <br/> |" \< PidTagCompanyName \> "  <br/> |
|0x00008017  <br/> |" \< PidTagSurname \> , space \< \> \< PidTagGivenName space \> \< \> \< PidTagMiddleName \> "  <br/> |
|0x00008018  <br/> |" \< PidTagCompanyName \> \r\n \< PidTagSurname \> , space \< \> \< PidTagGivenName space \> \< \> \< PidTagMiddleName \> "  <br/> |
|0x00008019  <br/> |" \< PidTagSurname \> , space \< \> \< PidTagGivenName space \> \< \> \< PidTagMiddleName \> \r\n \< PidTagCompanyName \> "  <br/> |
|0x00008030  <br/> |" \< PidTagSurname \> \< PidTagGivenName \> \< space \> \< PidTagMiddleName \> "  <br/> |
|0x00008031  <br/> |" \< PidTagSurname \> \< space \> \< PidTagGivenName \> \< space \> \< PidTagMiddleName \> "  <br/> |
|0x00008032  <br/> |" \< PidTagCompanyName \> \r\n \< PidTagSurname \> \< PidTagGivenName \> \< space \> \< PidTagMiddleName \> "  <br/> |
|0x00008033  <br/> |" \< PidTagCompanyName \> \r\n \< PidTagSurname \> \< space \> \< PidTagGivenName \> \< space \> \< PidTagMiddleName \> "  <br/> |
|0x00008034  <br/> |" \< PidTagSurname \> \< PidTagGivenName \> \< space \> \< PidTagMiddleName \> \r\n \< PidTagCompanyName \> "  <br/> |
|0x00008035  <br/> |" \< PidTagSurname \> \< space \> \< PidTagGivenName \> \< space \> \< PidTagMiddleName \> \r\n \< PidTagCompanyName \> "  <br/> |
|0x00008036  <br/> |" \< PidTagSurname \> \< space \> \< PidTagGivenName \> \< space \> \< PidTagMiddleName space \> \< \> \< PidTagGeneration \> "  <br/> |
|0x00008037  <br/> |" \< PidTagGivenName \> \< space \> \< PidTagMiddleName \> \< space \> \< PidTagSurname space \> \< \> \< PidTagGeneration \> "  <br/> |
|0x00008038  <br/> |" \< PidTagSurname \> \< PidTagGivenName \> \< space \> \< PidTagMiddleName \> \< space \> \< PidTagGeneration \> "  <br/> |
|0xfffffffd  <br/> |Especifica que, ao exibir o contato, o aplicativo deve tentar usar o valor atual **de dispidFileUnder** e outras propriedades de contato para encontrar uma "melhor combinação" para **dispidFileUnderId** para um dos valores anteriores nesta tabela.  <br/> |
|0xfffffffe  <br/> |Especifica que, ao exibir o contato, o aplicativo deve escolher os valores padrão apropriados (de acordo com a localidade do idioma) para **dispidFileUnderId** e atualizar **dispidFileUnder** para corresponder à escolha.  <br/> |
|0xffffffff  <br/> |**dispidFileUnder** é um PT_UNICODE fornecido pelo usuário e não deve ser alterado quando outra propriedade de nome de contato é alterada.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica as propriedades e operações permitidas para contatos e listas de distribuição pessoais.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

