---
title: Sobre URLs MAPI para indexação baseada em notificação
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9cb35f0a-267e-2d85-1701-02d52578a0b8
description: 'Modificado pela última vez: 08 de novembro de 2011'
ms.openlocfilehash: 27ad80b9eca8332beeda147a8b2b4204f9f1cd38
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766085"
---
# <a name="about-mapi-urls-for-notification-based-indexing"></a>Sobre URLs MAPI para indexação baseada em notificação

**Aplica-se a**: Outlook 
  
Quando um provedor de armazenamento notifica um indexador que um objeto está pronto para indexação, ela gerará uma URL de MAPI que identifica exclusivamente o objeto para o manipulador de protocolo de MAPI. URLs de MAPI são codificados em Unicode e ter o seguinte formato: 
  
`Mapi://SID/StoreDisplayName ($HashNumber)/StoreType/FolderNameA/…/FolderNameN/[EntryIDEncoded[/at=AttachIDEncoded:FileName]]`

A tabela a seguir descreve as várias partes de uma URL típica.

|Parte | Descrição|
|:----|:-----------|  
|*SID* |Identificador de segurança do usuário atual.| 
|*StoreDisplayName* |Uma cadeia de caracteres que especifica o nome para exibição do usuário desse repositório.|
|*HashNumber* |Um **DWORD** na representação hexadecimal que é calculada com base na identificação de entrada do repositório ou a assinatura de mapeamento do repositório. Esse valor é armazenado no registro e será usado posteriormente para identificar o repositório no manipulador de protocolo de MAPI.<br/><br/>Esse número deve ser calculado de uma forma que minimiza colisões com outros repositórios. Para o algoritmo que o Microsoft Outlook usa para calcular o número de hash, consulte o [algoritmo para calcular o número de Hash de repositório](algorithm-to-calculate-the-store-hash-number.md).|
|*StoreType* |Um número que identifica o tipo do repositório que contém o objeto a ser indexado. Os valores possíveis são:<br/>Repositório de - 0 - padrão.<br/><br/>-1 - repositório de representante, usado para itens de representante armazenados em cache localmente.<br/><br/>-2 - pastas públicas, usados para a pasta pública Favoritos.<br/><br/>**Observação**: se o repositório está sendo rastreado, em vez de enviados, o valor que é usado é o caractere*X*.| 
|*FolderNameA/.../FolderNameN* |O caminho da raiz do IPM_SUBTREE até a pasta ou mensagem. Por exemplo, uma mensagem na pasta **família** sob a **caixa de entrada** **tem/Família de caixa de entrada** para esse parâmetro. |
|*EntryIDEncoded* |Identificação de entrada MAPI para o item codificada como uma cadeia de caracteres Unicode. Consulte a seção a seguir "Caracteres especiais" para obter informações sobre como determinados caracteres especiais são codificados. Para obter mais informações sobre o algoritmo para codificar a identificação de entrada, consulte [algoritmo para codificar identificações de entrada e anexos](algorithm-to-encode-entry-ids-and-attachment-ids.md).<br/><br/>**Observação**: quando exibidos como texto, isso codificado entrada ID aparece como aleatório caracteres em Hangul ou caixas em conformidade com o algoritmo, dependendo de fontes disponíveis.  |
|*AttachIDEncoded* |ID de anexo codificado como uma cadeia de caracteres Unicode. Consulte a seção a seguir "Caracteres especiais" para obter informações sobre como determinados caracteres especiais são codificados. Para obter mais informações sobre o algoritmo para codificar a identificação de entrada, consulte [algoritmo para codificar identificações de entrada e anexos](algorithm-to-encode-entry-ids-and-attachment-ids.md).<br/><br/>**Observação**: quando exibidos como texto, isso codificado entrada ID aparece como aleatório caracteres em Hangul ou caixas em conformidade com o algoritmo, dependendo de fontes disponíveis. |
|*FileName* |Nome do anexo de arquivo, como ele aparece na mensagem.|
    
## <a name="examples-of-mapi-urls"></a>Exemplos de URLs MAPI

A seguir estão alguns exemplos de URLs de MAPI.
  
- URL de MAPI para uma pasta: 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($be19928f)/2/Office`
    
- URL de MAPI para uma mensagem: 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($484efb89)/0/Calendar/곯가가가걍걝걌곌겷걢곒갑겛개가검걟곔걙곾걤곂갠가`
    
- URL de MAPI para um anexo: 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($484efb89)/0/Inbox/곯가가가걍걝걌곌겷걢곒갑겛개가검걟곔걙곾간곷갦가/at=겅걋각가:somefile.txt`
    
## <a name="special-characters"></a>Caracteres especiais

Determinados caracteres são codificados caso apareçam na mensagem ou no anexo. O exemplo a seguir mostra quais caracteres são codificados em uma URL de MAPI:
  
- % > % 25
    
- / > % 2F 
    
- \ > %5c 
    
- \*> % 2A 
    
- ? > % 3F 
    
## <a name="blob-associated-with-each-mapi-url"></a>Blob associado a cada URL de MAPI

Quando envio uma URL de MAPI para um objeto a ser indexado, um provedor de armazenamento também cria um objeto binário grande (BLOB) que contém determinadas informações para o manipulador de protocolo de MAPI. O provedor de armazenamento associa esta BLOB cada URL MAPI e o envia ao envio a URL de MAPI para o indexador. O formato do BLOB é da seguinte maneira: 
  
```cpp
DWORD  dwVersion
DWORD  dwFlags
ULONG  cbProfileName
WCHAR  wszProfileName
ULONG  cbProviderItemID
WCHAR  wszProviderItemID
```

O provedor de armazenamento deve gravar esses valores BLOB na ordem mostrada. A tabela a seguir descreve cada campo do BLOB.

|Parte | Descrição|
|:----|:-----------|  
|*dwVersion* |Esta é a versão dos dados que estão sendo enviadas. No momento, esse valor é 1.|
|*dwFlags* |Reservado para uso futuro. No momento, esse valor deve ser 0.|
|*cbProfileName* |O tamanho do nome do perfil, em bytes. Essa informação é útil para o manipulador de protocolo MAPI saber qual perfil a ser usado quando o item de indexação.|
|*wszProfileName* |Terminada em nulo Unicode cadeia de caracteres que contém o nome de perfil.|
|*cbProviderItemID* |Tamanho da identificação de item do provedor, em bytes. O provedor de armazenamento deve enviar apenas o provedor de ID de item para pastas, para evitar abrindo pastas adicionais para obter essas informações.|
|*wszProviderItemID* |Cadeia de Unicode terminada em nulo, com a ID de item de provedor que identifica exclusivamente o item no repositório.|
    
## <a name="see-also"></a>Confira também

- [Sobre a indexação do repositório baseada em notificação](about-notification-based-store-indexing.md)
- [Constantes MAPI](mapi-constants.md)

