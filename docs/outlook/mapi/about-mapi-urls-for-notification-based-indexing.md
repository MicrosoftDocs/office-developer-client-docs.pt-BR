---
title: Sobre URLs MAPI para Notification-Based indexação
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9cb35f0a-267e-2d85-1701-02d52578a0b8
description: 'Last modified: November 08, 2011'
ms.openlocfilehash: 5a3e45809f36b71968560a4b239e268addf00474
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422478"
---
# <a name="about-mapi-urls-for-notification-based-indexing"></a>Sobre URLs MAPI para Notification-Based indexação

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Quando um provedor de armazenamento notifica um indexador de que um objeto está pronto para indexação, ele gera uma URL MAPI que identifica exclusivamente o objeto para o Manipulador de Protocolo MAPI. AS URLs MAPI são codificadas em Unicode e têm o seguinte formato: 
  
`Mapi://SID/StoreDisplayName ($HashNumber)/StoreType/FolderNameA/…/FolderNameN/[EntryIDEncoded[/at=AttachIDEncoded:FileName]]`

A tabela a seguir descreve as várias partes de uma URL típica.

|Sair | Descrição|
|:----|:-----------|  
|*SID* |O identificador de segurança do usuário atual.| 
|*StoreDisplayName* |Uma cadeia de caracteres que especifica o nome de exibição do usuário nesse armazenamento.|
|*HashNumber* |Uma **DWORD** em representação hexadecimal calculada com base na ID de entrada do armazenamento ou na assinatura de mapeamento do armazenamento. Esse valor é armazenado no Registro e será usado posteriormente para identificar o armazenamento no Manipulador de Protocolo MAPI.<br/><br/>Esse número deve ser calculado de forma a minimizar colisões com outros armazenamentos. Para o algoritmo que o Microsoft Outlook usa para calcular o número de hash, consulte [Algoritmo para calcular o número de hash da Loja.](algorithm-to-calculate-the-store-hash-number.md)|
|*StoreType* |Um número que identifica o tipo do armazenamento que contém o objeto a ser indexado. Os valores possíveis são os seguintes:<br/>- 0 - Armazenamento padrão.<br/><br/>- 1 - Armazenamento de representante, usado para itens de representante armazenados em cache localmente.<br/><br/>- 2 - Pastas públicas, usadas para favoritos de pasta pública.<br/><br/>**OBSERVAÇÃO:** se o armazenamento estiver sendo rastreado em vez de pressionado, o valor usado será o caractere *X*.| 
|*FolderNameA/.../FolderNameN* |O caminho da raiz do IPM_SUBTREE para a pasta ou mensagem. Por exemplo, uma mensagem na pasta **Família** em **Caixa** de Entrada tem Caixa **de Entrada/Família** para esse parâmetro. |
|*EntryIDEncoded* |ID de entrada MAPI do item codificado como uma cadeia de caracteres Unicode. Consulte a seção "Caracteres especiais" a seguir para obter informações sobre como determinados caracteres especiais são codificados. Para obter mais informações sobre o algoritmo para codificar a ID de entrada, consulte Algoritmo para codificar IDs de entrada [e IDs de anexo.](algorithm-to-encode-entry-ids-and-attachment-ids.md)<br/><br/>**OBSERVAÇÃO:** quando visualizada como texto, essa ID de entrada codificada aparece como caixas ou caracteres hangul aleatórios em conformidade com o algoritmo, dependendo das fontes disponíveis.  |
|*AttachIDEncoded* |ID do anexo codificado como uma cadeia de caracteres Unicode. Consulte a seção "Caracteres especiais" a seguir para obter informações sobre como determinados caracteres especiais são codificados. Para obter mais informações sobre o algoritmo para codificar a ID de entrada, consulte Algoritmo para codificar IDs de entrada [e IDs de anexo.](algorithm-to-encode-entry-ids-and-attachment-ids.md)<br/><br/>**OBSERVAÇÃO:** quando visualizada como texto, essa ID de entrada codificada aparece como caixas ou caracteres hangul aleatórios em conformidade com o algoritmo, dependendo das fontes disponíveis. |
|*FileName* |Nome do arquivo de anexo, como ele aparece na mensagem.|
    
## <a name="examples-of-mapi-urls"></a>Exemplos de URLs MAPI

A seguir estão alguns exemplos de URLs MAPI.
  
- URL MAPI de uma pasta: 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($be19928f)/2/Office`
    
- URL MAPI de uma mensagem: 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($484efb89)/0/Calendar/곯가가가걍걝걌곌겷걢곒갑겛개가검걟곔걙곾걤곂갠가`
    
- URL MAPI para um anexo: 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($484efb89)/0/Inbox/곯가가가걍걝걌곌겷걢곒갑겛개가검걟곔걙곾간곷갦가/at=겅걋각가:somefile.txt`
    
## <a name="special-characters"></a>Caracteres especiais

Determinados caracteres são codificados se aparecerem na mensagem ou no anexo. Veja a seguir quais caracteres são codificados em uma URL MAPI:
  
- % > %25
    
- / > %2F 
    
- \ > %5C 
    
- \* > %2A 
    
- ? > %3F 
    
## <a name="blob-associated-with-each-mapi-url"></a>Blob associado a cada URL MAPI

Ao pressionar uma URL MAPI para um objeto a ser indexado, um provedor de armazenamento também cria um BLOB (objeto binário grande) que contém determinadas informações para o Manipulador de Protocolo MAPI. O provedor de armazenamento associa esse BLOB a cada URL MAPI e o envia ao enviar a URL MAPI para o indexador. O formato do BLOB é o seguinte: 
  
```cpp
DWORD  dwVersion
DWORD  dwFlags
ULONG  cbProfileName
WCHAR  wszProfileName
ULONG  cbProviderItemID
WCHAR  wszProviderItemID
```

O provedor de armazenamento deve gravar esses valores no BLOB na ordem mostrada. A tabela a seguir descreve cada campo do BLOB.

|Sair | Descrição|
|:----|:-----------|  
|*dwVersion* |Esta é a versão dos dados que estão sendo enviados. Atualmente, esse valor é 1.|
|*dwFlags* |Reserved for future use. Atualmente, esse valor deve ser 0.|
|*cbProfileName* |O tamanho do nome do perfil, em bytes. Essas informações são úteis para o Manipulador de Protocolo MAPI saber qual perfil usar ao indexar o item.|
|*wszProfileName* |Cadeia de caracteres Unicode terminada por caractere nulo que contém o nome do perfil.|
|*cbProviderItemID* |Tamanho da ID do item do provedor, em bytes. O provedor de armazenamento deve enviar apenas a ID do item do provedor para pastas, para impedir a abertura de pastas adicionais para obter essas informações.|
|*wszProviderItemID* |Cadeia de caracteres Unicode terminada por caractere nulo com a ID do item do provedor que identifica exclusivamente o item no armazenamento.|
    
## <a name="see-also"></a>Confira também

- [Sobre Notification-Based Store Indexação](about-notification-based-store-indexing.md)
- [Constantes de MAPI](mapi-constants.md)

