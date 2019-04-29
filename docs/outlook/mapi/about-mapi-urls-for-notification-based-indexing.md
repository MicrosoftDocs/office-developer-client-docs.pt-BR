---
title: Sobre URLs MAPI para indexação baseada em notificação
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9cb35f0a-267e-2d85-1701-02d52578a0b8
description: 'Última modificação: 08 de novembro de 2011'
ms.openlocfilehash: 5a3e45809f36b71968560a4b239e268addf00474
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422478"
---
# <a name="about-mapi-urls-for-notification-based-indexing"></a>Sobre URLs MAPI para indexação baseada em notificação

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Quando um provedor de armazenamento notifica um indexador de que um objeto está pronto para indexação, ele gera uma URL MAPI que identifica exclusivamente o objeto para o manipulador de protocolo MAPI. As URLs de MAPI são codificadas em Unicode e têm o seguinte formato: 
  
`Mapi://SID/StoreDisplayName ($HashNumber)/StoreType/FolderNameA/…/FolderNameN/[EntryIDEncoded[/at=AttachIDEncoded:FileName]]`

A tabela a seguir descreve as várias partes de uma URL típica.

|Sair | Descrição|
|:----|:-----------|  
|*Identifica* |O identificador de segurança do usuário atual.| 
|*StoreDisplayName* |Uma cadeia de caracteres que especifica o nome de exibição do usuário no repositório.|
|*HashNumber* |Uma **DWORD** em representação hexadecimal que é calculada com base na ID de entrada da loja ou na assinatura de mapeamento de repositório. Esse valor é armazenado no registro e será usado posteriormente para identificar o repositório no manipulador de protocolo MAPI.<br/><br/>Esse número deve ser calculado de uma forma que minimize as colisões com outras lojas. Para o algoritmo que o Microsoft Outlook usa para calcular o número de hash, confira [algoritmo para calcular o número de hash do repositório](algorithm-to-calculate-the-store-hash-number.md).|
|*StoreType* |Um número que identifica o tipo de armazenamento que contém o objeto a ser indexado. Os valores possíveis são os seguintes:<br/>-0-repositório padrão.<br/><br/>-1-repositório de representante, usado para itens delegados armazenados em cache localmente.<br/><br/>-2-pastas públicas, usadas para a pasta pública favoritos.<br/><br/>**Observação**: se o repositório estiver sendo rastreado em vez de enviado, o valor usado será o caractere*X*.| 
|*Nome_da_pastaa/.../nome_da_pasta* |O caminho da raiz do IPM_SUBTREE para a pasta ou a mensagem. Por exemplo, uma mensagem na pasta **família** em **caixa de entrada** tem **caixa de entrada/família** para esse parâmetro. |
|*EntryIDEncoded* |ID de entrada MAPI para o item codificado como uma cadeia de caracteres Unicode. Consulte a seção "caracteres especiais" a seguir para obter informações sobre como determinados caracteres especiais são codificados. Para obter mais informações sobre o algoritmo para codificar a identificação de entrada, confira [algoritmo para codificar IDs de entrada e IDs de anexo](algorithm-to-encode-entry-ids-and-attachment-ids.md).<br/><br/>**Observação**: quando exibido como texto, essa ID de entrada codificada aparece como caracteres Hangul aleatórios ou caixas em conformidade com o algoritmo, dependendo das fontes disponíveis.  |
|*AttachIDEncoded* |ID de anexo codificada como uma cadeia de caracteres Unicode. Consulte a seção "caracteres especiais" a seguir para obter informações sobre como determinados caracteres especiais são codificados. Para obter mais informações sobre o algoritmo para codificar a identificação de entrada, confira [algoritmo para codificar IDs de entrada e IDs de anexo](algorithm-to-encode-entry-ids-and-attachment-ids.md).<br/><br/>**Observação**: quando exibido como texto, essa ID de entrada codificada aparece como caracteres Hangul aleatórios ou caixas em conformidade com o algoritmo, dependendo das fontes disponíveis. |
|*FileName* |Nome do arquivo de anexo, como aparece na mensagem.|
    
## <a name="examples-of-mapi-urls"></a>Exemplos de URLs de MAPI

Veja a seguir alguns exemplos de URLs de MAPI.
  
- URL MAPI de uma pasta: 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($be19928f)/2/Office`
    
- URL MAPI para uma mensagem: 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($484efb89)/0/Calendar/곯가가가걍걝걌곌겷걢곒갑겛개가검걟곔걙곾걤곂갠가`
    
- URL MAPI de um anexo: 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($484efb89)/0/Inbox/곯가가가걍걝걌곌겷걢곒갑겛개가검걟곔걙곾간곷갦가/at=겅걋각가:somefile.txt`
    
## <a name="special-characters"></a>Caracteres especiais

Determinados caracteres serão codificados se aparecerem na mensagem ou no anexo. O seguinte mostra quais caracteres são codificados em uma URL MAPI:
  
- % >% 25
    
- />% 2F 
    
- \ >% 5C 
    
- \*>% 2A 
    
- ? >% 3F 
    
## <a name="blob-associated-with-each-mapi-url"></a>Blob associado a cada URL MAPI

Ao estender uma URL MAPI para um objeto a ser indexado, um provedor de repositório também cria um objeto binário grande (BLOB) que contém determinadas informações para o manipulador de protocolo MAPI. O provedor de repositório associa este BLOB a cada URL MAPI e o envia ao enviar a URL MAPI para o indexador. O formato do BLOB é o seguinte: 
  
```cpp
DWORD  dwVersion
DWORD  dwFlags
ULONG  cbProfileName
WCHAR  wszProfileName
ULONG  cbProviderItemID
WCHAR  wszProviderItemID
```

O provedor de repositório deve gravar esses valores no BLOB na ordem mostrada. A tabela a seguir descreve cada campo do BLOB.

|Sair | Descrição|
|:----|:-----------|  
|*dwVersion* |Esta é a versão dos dados que estão sendo enviados. No momento, esse valor é 1.|
|*dwFlags* |Reserved for future use. No momento, esse valor deve ser 0.|
|*cbProfileName* |O tamanho do nome do perfil, em bytes. Essas informações são úteis para que o manipulador de protocolo MAPI saiba qual perfil usar ao indexar o item.|
|*wszProfileName* |Cadeia de caracteres Unicode terminada em nulo que contém o nome do perfil.|
|*cbProviderItemID* |Tamanho da ID do item do provedor, em bytes. O provedor de repositório deve enviar somente a ID de item de provedor para pastas, para evitar a abertura de pastas adicionais para obter essas informações.|
|*wszProviderItemID* |Cadeia de caracteres Unicode terminada em nulo com a ID de item do provedor que identifica exclusivamente o item no repositório.|
    
## <a name="see-also"></a>Confira também

- [Sobre a indexação de repositórios baseados em notificação](about-notification-based-store-indexing.md)
- [Constantes de MAPI](mapi-constants.md)

