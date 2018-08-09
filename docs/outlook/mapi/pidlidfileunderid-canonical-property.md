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
ms.openlocfilehash: 08e2403be35b87393d22f9109f59c0572c53073b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768482"
---
# <a name="pidlidfileunderid-canonical-property"></a>Propriedade canônica PidLidFileUnderId

  
  
**Aplica-se a**: Outlook 
  
Especifica como gerar e recalcular o valor da propriedade **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) quando alterar propriedades de nome de outro contato.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidFileUnderId  <br/> |
|Propriedade definida:  <br/> |PSETID_Address  <br/> |
|ID de longo (LID):  <br/> |0x00008006  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Contato  <br/> |
   
## <a name="remarks"></a>Comentários

Se essa propriedade estiver faltando ou definida como um valor que não são detalhado na tabela a seguir ou em [[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx), o aplicativo pode escolher sua própria lógica recalcular o valor do **dispidFileUnder** como outra alteração de propriedades do nome do contato. 
  
Na tabela a seguir, a notação <PropertyName> é usado para especificar "o valor de PropertyName". Por exemplo, se o valor da propriedade **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md)) é "Smith", e o valor da propriedade **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) é "Ben", em seguida, "<PidTagGivenName> <PidTagSurname>" Especifica a cadeia de caracteres "Ben Smith". Na tabela, "\r" Especifica um caractere de retorno de carro, "\n." Especifica um caractere de alimentação de linha, e <space> representa um caractere de espaço.
  
|**Valor da propriedade **dispidFileUnderId****|**Descrição da propriedade **dispidFileUnder****|
|:-----|:-----|
|0x00000000  <br/> |PT_UNICODE vazia.  <br/> |
|0x00003001  <br/> |"\<PidTagDisplayName\>"  <br/> |
|0x00003A06  <br/> |"\<PidTagGivenName\>"  <br/> |
|0x00003A11  <br/> |"\<PidTagSurname\>"  <br/> |
|0x00003A16  <br/> |"\<PidTagCompanyName\>"  <br/> |
|0x00008017  <br/> |"\<PidTagSurname\>,\<espaço\>\<PidTagGivenName\>\<espaço\>\<PidTagMiddleName\>"  <br/> |
|0x00008018  <br/> |"\<PidTagCompanyName\>\r\n\<PidTagSurname\>,\<espaço\>\<PidTagGivenName\>\<espaço\>\<PidTagMiddleName\>"  <br/> |
|0x00008019  <br/> |"\<PidTagSurname\>,\<espaço\>\<PidTagGivenName\>\<espaço\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"  <br/> |
|0x00008030  <br/> |"\<PidTagSurname\>\<PidTagGivenName\>\<espaço\>\<PidTagMiddleName\>"  <br/> |
|0x00008031  <br/> |"\<PidTagSurname\>\<espaço\>\<PidTagGivenName\>\<espaço\>\<PidTagMiddleName\>"  <br/> |
|0x00008032  <br/> |"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<PidTagGivenName\>\<espaço\>\<PidTagMiddleName\>"  <br/> |
|0x00008033  <br/> |"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<espaço\>\<PidTagGivenName\>\<espaço\>\<PidTagMiddleName\>"  <br/> |
|0x00008034  <br/> |"\<PidTagSurname\>\<PidTagGivenName\>\<espaço\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"  <br/> |
|0x00008035  <br/> |"\<PidTagSurname\>\<espaço\>\<PidTagGivenName\>\<espaço\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"  <br/> |
|0x00008036  <br/> |"\<PidTagSurname\>\<espaço\>\<PidTagGivenName\>\<espaço\>\<PidTagMiddleName\>\<espaço\>\<PidTagGeneration\>"  <br/> |
|0x00008037  <br/> |"\<PidTagGivenName\>\<espaço\>\<PidTagMiddleName\>\<espaço\>\<PidTagSurname\>\<espaço\>\<PidTagGeneration\>"  <br/> |
|0x00008038  <br/> |"\<PidTagSurname\>\<PidTagGivenName\>\<espaço\>\<PidTagMiddleName\>\<espaço\>\<PidTagGeneration\>"  <br/> |
|0xfffffffd  <br/> |Especifica que, ao exibir o contato, o aplicativo deve tentar usar o valor atual do **dispidFileUnder** e outras propriedades de contato para encontrar uma "melhor correspondência" para **dispidFileUnderId** para um dos valores anteriores nesta tabela.  <br/> |
|0xFFFFFFFE  <br/> |Especifica que, ao exibir o contato, o aplicativo deve escolher os valores padrão adequado (de acordo com a localidade do idioma) para **dispidFileUnderId** e **dispidFileUnder** para coincidir com a opção de atualização.  <br/> |
|0xFFFFFFFF  <br/> |**dispidFileUnder** é um PT_UNICODE fornecido pelo usuário e não deve ser alterado quando outra propriedade de nome do contato é alterada.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.
    
[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas para contatos e listas de distribuição pessoal.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

