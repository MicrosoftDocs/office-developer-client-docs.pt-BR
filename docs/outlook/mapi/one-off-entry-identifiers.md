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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279686"
---
# <a name="one-off-entry-identifiers"></a>Identificadores de entradas únicas
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os identificadores de entrada únicos são criados por MAPI no método **IAddrBook:: CreateOneOff** e por componentes que não têm acesso ao subsistema MAPI, como componentes de gateway. Para obter mais informações, consulte [IAddrBook:: CreateOneOff](iaddrbook-createoneoff.md). A ilustração a seguir mostra o formato de um identificador de entrada one-off.
  
**One-off entry identifier format**
  
![Formato de identificador de entrada one-off] (media/amapi_69.gif "Formato de identificador de entrada one-off")
  
O primeiro campo é uma estrutura especial do [MAPIUID](mapiuid.md) que identifica o identificador de entrada como a representação de um destinatário personalizado. Esta estrutura **MAPIUID** deve ser definida como a constante MAPI_ONE_OFF_UID. MAPI_ONE_OFF_UID é definido no arquivo de cabeçalho MAPIDEFS. 0. 
  
Os campos Version e flags são palavras de 16 bits na ordem de bytes da Intel. O campo Version deve ser definido como zero. O campo Flags pode ser definido com os seguintes valores:
  
MAPI_ONE_OFF_NO_RICH_INFO
  
MAPI_ONE_OFF_UNICODE
  
O sinalizador MAPI_ONE_OFF_NO_RICH_INFO é definido se um destinatário não deve receber o conteúdo da mensagem no formato de encapsulamento neutro de transporte (TNEF). Este sinalizador é definido quando MAPI_SEND_NO_RICH_INFO é passado para o método [IAddrBook:: CreateOneOff](iaddrbook-createoneoff.md) . 
  
O sinalizador MAPI_ONE_OFF_UNICODE é definido se o nome de exibição e o endereço de email são cadeias de caracteres Unicode. Este sinalizador é definido quando o MAPI_UNICODE é passado para **IAddrBook:: CreateOneOff**. Quando o sinalizador MAPI_UNICODE não é passado para **CreateOneOff**, o MAPI pressupõe que o nome de exibição e as cadeias de endereço de email estão no conjunto de caracteres ANSI atual da estação de trabalho. As cadeias de caracteres ANSI geralmente não funcionam bem em mensagens que são enviadas entre plataformas usando conjuntos de caracteres diferentes porque a página de código não é codificada no identificador de entrada. Para proteger contra essa incompatibilidade em potencial, vários tipos de endereço são limitados apenas aos caracteres comuns em vários conjuntos de caracteres. No enTanto, para garantir a compatibilidade de conjunto de caracteres e plataforma, os clientes devem usar Unicode para as cadeias de caracteres em suas mensagens.
  
O nome para exibição é uma cadeia de caracteres terminada em nulo que corresponde à propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) do destinatário e ao parâmetro _lpszName_ passado para **IAddrBook:: CreateOneOff**. O conjunto de caracteres será Unicode se o sinalizador MAPI_ONE_OFF_UNICODE estiver definido e ANSI se estiver claro. 
  
O tipo de endereço é uma cadeia de caracteres terminada em nulo que corresponde à propriedade **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) do destinatário e ao parâmetro _lpszAdrType_ passado para **IAddrBook:: CreateOneOff**. 
  
O endereço de email é uma cadeia de caracteres terminada em nulo que corresponde à propriedade **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) do destinatário e ao parâmetro _lpszAddress_ passado para **IAddrBook:: CreateOneOff**. 
  
> [!NOTE]
> Não há nenhum preenchimento nas estruturas de identificador de entrada one-off; os bytes são empacotados exatamente como indicado acima e o comprimento do identificador de entrada não deve incluir nenhum byte além do caractere nulo de terminação do endereço de email. 
  
Os clientes e provedores de catálogo de endereços que criam manualmente identificadores de entrada únicos também podem precisar gerar valores para as propriedades **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) e **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)). A chave de registro é idêntica ao identificador de entrada. A chave de pesquisa deve ser formada com a concatenação dos seguintes campos na seguinte ordem:
  
1. O tipo de endereço, convertido em caracteres maiúsculos.
    
2. Dois-pontos (:).
    
3. O endereço de email, convertido em caracteres maiúsculos.
    
4. Um caractere nulo de terminação.
    
Nenhuma conversão de conjunto de caracteres deve ser feita ao gerar a chave de pesquisa.
  

