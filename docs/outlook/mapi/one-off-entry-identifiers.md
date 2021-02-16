---
title: Identificadores de entradas únicas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 741d21ae-f14a-4b7f-80aa-91d0f0ff3f34
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: abe52cb45e13e6713d28fffe379e245e2483bffa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411040"
---
# <a name="one-off-entry-identifiers"></a>Identificadores de entradas únicas
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Identificadores de entrada único são criados por MAPI no método **IAddrBook::CreateOneOff** e por componentes que não têm acesso ao subsistema MAPI, como componentes de gateway. Para obter mais informações, consulte [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md). A ilustração a seguir mostra o formato de um identificador de entrada único.
  
**One-off entry identifier format**
  
![Formato de identificador de entrada]único formato(media/amapi_69.gif "de identificador de entrada único")
  
O primeiro campo é uma estrutura [MAPIUID](mapiuid.md) especial que identifica o identificador de entrada como representando um destinatário personalizado. Essa **estrutura MAPIUID** deve ser definida como a constante MAPI_ONE_OFF_UID. MAPI_ONE_OFF_UID é definido no arquivo de header MAPIDEFS.H. 
  
Os campos de versão e sinalizadores são palavras de 16 bits na ordem de byte intel. O campo de versão deve ser definido como zero. O campo de sinalizadores pode ser definido com os seguintes valores:
  
MAPI_ONE_OFF_NO_RICH_INFO
  
MAPI_ONE_OFF_UNICODE
  
O MAPI_ONE_OFF_NO_RICH_INFO padrão é definido se um destinatário não deve receber conteúdo de mensagem no TNEF (Transport Neutral Encapsulation Format). Esse sinalizador é definido quando MAPI_SEND_NO_RICH_INFO é passado para [o método IAddrBook::CreateOneOff.](iaddrbook-createoneoff.md) 
  
O MAPI_ONE_OFF_UNICODE padrão será definido se o nome de exibição e o endereço de email são cadeias de caracteres Unicode. Esse sinalizador é definido quando o MAPI_UNICODE é passado para **IAddrBook::CreateOneOff**. Quando o MAPI_UNICODE sinalizador não é passado para **CreateOneOff**, o MAPI pressupo que o nome de exibição e as cadeias de caracteres de endereço de email estão no conjunto de caracteres ANSI atual da estação de trabalho. Cadeias de caracteres ANSI geralmente não funcionam bem em mensagens enviadas entre plataformas usando conjuntos de caracteres diferentes porque a página de código não é codificada no identificador de entrada. Para se proteger contra essa incompatibilidade em potencial, muitos tipos de endereços são limitados apenas aos caracteres que são comuns em vários conjuntos de caracteres. No entanto, para garantir o conjunto de caracteres e a compatibilidade da plataforma, os clientes devem usar Unicode para as cadeias de caracteres em suas mensagens.
  
O nome de exibição é uma cadeia de caracteres terminada em nulo que corresponde à propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) do destinatário e ao parâmetro  _lpszName_ passado para **IAddrBook::CreateOneOff**. O conjunto de caracteres será Unicode se o sinalizador MAPI_ONE_OFF_UNICODE estiver definido e ANSI se estiver claro. 
  
O tipo de endereço é uma cadeia de caracteres terminada em nulo que corresponde à propriedade **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) do destinatário e ao parâmetro  _lpszAdrType_ passado para **IAddrBook::CreateOneOff**. 
  
O endereço de email é uma cadeia de caracteres terminada em nulo que corresponde à propriedade **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) do destinatário e ao parâmetro  _lpszAddress_ passado para **IAddrBook::CreateOneOff**. 
  
> [!NOTE]
> Não há preenchimento em estruturas de identificador de entrada única; os bytes são empacotados exatamente como indicado acima e o comprimento do identificador de entrada não deve incluir nenhum bytes além do caractere nulo final do endereço de email. 
  
Clientes e provedores de livro de endereços que construam manualmente identificadores de entrada únicas também podem precisar gerar valores para as propriedades **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) e **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) . A tecla de registro é idêntica ao identificador de entrada. A chave de pesquisa deve ser formada concatenando os seguintes campos na seguinte ordem:
  
1. O tipo de endereço, convertido em caracteres em maiúsculas.
    
2. Dois-pontos (:).
    
3. O endereço de email, convertido em caracteres em maiúsculas.
    
4. Um caractere nulo de terminação.
    
Nenhuma conversão de conjunto de caracteres deve ser feita ao gerar a chave de pesquisa.
  

