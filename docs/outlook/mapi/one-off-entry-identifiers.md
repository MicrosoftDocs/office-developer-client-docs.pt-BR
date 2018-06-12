---
title: Identificadores de entrada únicos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 741d21ae-f14a-4b7f-80aa-91d0f0ff3f34
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 1335de3c1decf6c594f0148fbbf055061d7ce7e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768162"
---
# <a name="one-off-entry-identifiers"></a>Identificadores de entrada únicos
  
**Aplica-se a**: Outlook 
  
Identificadores de entrada únicos são criados por MAPI no método **IAddrBook::CreateOneOff** e componentes que não têm acesso ao subsistema de MAPI, como componentes do gateway. Para obter mais informações, consulte [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md). A ilustração a seguir mostra o formato de um identificador de entrada únicos.
  
**Formato do identificador de entrada únicos**
  
![Formato do identificador de entrada únicos] (media/amapi_69.gif "Formato do identificador de entrada únicos")
  
O primeiro campo é uma estrutura [MAPIUID](mapiuid.md) especial que identifica o identificador de entrada como representando um destinatário personalizado. Essa estrutura **MAPIUID** deve ser definida para a constante MAPI_ONE_OFF_UID. MAPI_ONE_OFF_UID é definida no arquivo de cabeçalho MAPIDEFS. H. 
  
Os campos de versão e os sinalizadores são palavras de 16 bits em ordem de bytes da Intel. Campo versão deverá ser definido como zero. O campo flags pode ser definido para os seguintes valores:
  
MAPI_ONE_OFF_NO_RICH_INFO
  
MAPI_ONE_OFF_UNICODE
  
O sinalizador MAPI_ONE_OFF_NO_RICH_INFO é definido se um destinatário não deve receber conteúdo da mensagem no TNEF Transport Neutral Encapsulation Format (). Esse sinalizador é definido quando MAPI_SEND_NO_RICH_INFO é passado ao método [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) . 
  
O sinalizador MAPI_ONE_OFF_UNICODE é definido se a exibição nome e endereço de email é cadeias de caracteres Unicode. Esse sinalizador é definido quando o MAPI_UNICODE é passado para **IAddrBook::CreateOneOff**. Quando o sinalizador MAPI_UNICODE não é passado para **CreateOneOff**, MAPI pressupõe que as sequências de endereço de nome e email de exibição no conjunto de caracteres ANSI atual da estação de trabalho. Cadeias de caracteres ANSI geralmente não funcionam bem em mensagens que são enviadas entre plataformas usando diferentes conjuntos de caracteres, porque a página de código não é codificada o identificador de entrada. Para proteger contra essa incompatibilidade potencial, muitos tipos de endereço estão limitados a apenas esses caracteres que são comuns entre vários conjuntos de caracteres. No entanto, para garantir a compatibilidade de plataforma e conjunto de caracteres, os clientes devem usar Unicode para sequências de caracteres em suas mensagens.
  
O nome de exibição é uma cadeia de caracteres terminada em nulo que corresponde à propriedade de **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) do destinatário e ao parâmetro _lpszName_ passado para **IAddrBook::CreateOneOff**. O conjunto de caracteres é Unicode, se o sinalizador MAPI_ONE_OFF_UNICODE é definido e ANSI, se ele estiver desmarcado. 
  
O tipo de endereço é uma cadeia de caracteres terminada em nulo que corresponde à propriedade de **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) do destinatário e ao parâmetro _lpszAdrType_ passado para **IAddrBook::CreateOneOff**. 
  
O endereço de email é uma cadeia de caracteres terminada em nulo que corresponde à propriedade de **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) do destinatário e ao parâmetro _lpszAddress_ passado para **IAddrBook::CreateOneOff**. 
  
> [!NOTE]
> Não há nenhum preenchimento nas estruturas de identificador de entrada únicos; os bytes são compactados exatamente conforme indicado acima e o comprimento do identificador de entrada não deve incluir qualquer bytes além do caractere nulo de terminação do endereço de email. 
  
Clientes e provedores de catálogo de endereços que construir manualmente os identificadores de entrada únicos talvez também precise gerar valores para as propriedades de **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) e o **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)). A chave do registro é idêntica ao identificador de entrada. A chave de pesquisa deve ser formada concatenando os seguintes campos na seguinte ordem:
  
1. O tipo de endereço, convertido em caracteres maiusculos.
    
2. Dois-pontos (:).
    
3. O endereço de email é convertido em caracteres maiusculos.
    
4. Um caractere nulo de terminação.
    
Nenhuma conversão de conjunto de caracteres deve ser feito ao gerar a chave de pesquisa.
  

