---
title: Criando um anexo de mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 711b6765-7763-41ae-9ff8-61ca6ddd459d
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: eef42a8c7d19af313316bea68624ac67fb1ab4e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766358"
---
# <a name="creating-a-message-attachment"></a>Criando um anexo de mensagem
  
**Aplica-se a**: Outlook 
  
Um anexo da mensagem é alguns dados adicionais, como um arquivo, outra mensagem ou um objeto OLE, que você pode enviar ou salvar, juntamente com uma mensagem. Cada anexo tem um conjunto de propriedades que o identifica e descreve seu tipo e como ele é processado. Como destinatários, anexos de mensagens só podem ser acessados por meio da mensagem às quais eles pertencem. Portanto, para um anexo ser usado, sua mensagem deve estar aberta.
  
## <a name="create-a-message-attachment"></a>Criar um anexo da mensagem
  
1. Chame o método de [IMessage::CreateAttach](imessage-createattach.md) da mensagem e passe NULL como o identificador de interface. **CreateAttach** retorna um número que identifica exclusivamente o novo anexo dentro da mensagem. O número de anexo é armazenado na propriedade **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) e é válido apenas enquanto a mensagem contendo o anexo é aberta.
    
2. Chame [IMAPIProp::SetProps](imapiprop-setprops.md) para definir **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) para indicar como acessar o anexo. **PR_ATTACH_METHOD** é necessário. Defini-la como: 
    
   - ATTACH_BY_VALUE se o anexo é dados binários.
    
   - ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE ou ATTACH_BY_REF_ONLY se o anexo é um arquivo.
    
   - ATTACH_EMBEDDED_MSG se o anexo é uma mensagem.
    
   - ATTACH_OLE se o anexo é um objeto OLE.
    
3. Defina a propriedade de dados anexo apropriado:
    
   - **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) para dados binários e objetos OLE 1.
    
   - **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) para arquivos.
    
   - **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) para mensagens e objetos OLE 2.
    
4. Defina **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) para armazenar a representação gráfica do anexo de arquivo ou anexos binários. Não defini-la para os objetos OLE, qual armazenam as informações de renderização internamente, ou para mensagens anexadas. 
    
5. Defina **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) para indicar onde o anexo deve ser exibido. **PR_RENDERING_POSITION** se aplica apenas aos clientes que defina a propriedade **PR_BODY** . Caso você ofereça suporte somente **PR_RTF_COMPRESSED**, coloque as seguintes informações de espaço reservado no stream compactado:
    
   `\objattph`

   Para definir **PR_RENDERING_POSITION**, atribua um número que representa um deslocamento ordinal em caracteres, com o primeiro caractere da **PR_BODY** sendo 0, se você precisar saber onde na mensagem de que o anexo é processado ou 0xFFFFFFFF, se você não fizer isso processa anexos em **PR_BODY**.
    
6. Definir **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) para indicar o nome curto do arquivo para um anexo de arquivo e **PR\_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) para indicar o nome do arquivo como compatíveis em uma plataforma que processa o formato de nome de arquivo longo. Ambas as propriedades são opcionais. No entanto, se você definir **PR_ATTACH_LONG_FILENAME**, defina também **PR_ATTACH_FILENAME**. 
    
7. Defina **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) para indicar o nome do anexo que podem aparecer em uma caixa de diálogo. PR_DISPLAY_NAME é opcional. 
    
## <a name="set-prattachdatabin"></a>Definir PR_ATTACH_DATA_BIN
  
1. Chame [IMAPIProp::OpenProperty](imapiprop-openproperty.md) para abrir a propriedade com a interface **IStream** . 
    
2. Se um arquivo contém os dados e ele estiver aberto ou se você precisar controle explícito sobre o tamanho do buffer, chame **IStream::Write** em um loop para colocar os dados no stream. 
    
3. Outra opção é chamar **OpenStreamOnFile** para criar um fluxo para acessar o arquivo de dados e, em seguida, chame o método de **IStream::CopyTo** deste fluxo para copiar os dados para o fluxo retornado por **OpenProperty**.
    
4. Chame o método de **IStream::Commit** do novo do fluxo. 
    
## <a name="set-prattachdataobj"></a>Definir PR_ATTACH_DATA_OBJ
  
1. Chame **IMAPIProp::OpenProperty** para abrir a propriedade com a interface **IStreamDocfile** para criar um fluxo que funciona com armazenamento estruturado. **IStreamDocfile** é implementado por provedores de armazenamento de mensagem para oferecer uma maneira de alto desempenho para armazenar e recuperar o armazenamento estruturado de clientes. A interface **IStreamDocfile** é igual ao **IStream**, mas o conteúdo do fluxo é garantido a ser formatado como armazenamento estruturado. Se essa chamada tiver êxito, crie fluxo com as mesmas etapas descritas para a configuração **PR_ATTACH_DATA_BIN**.
    
2. Se **OpenProperty** falhar: 
    
   1. Chame **OpenProperty** solicitando **IStorage**novamente. 
      
   2. Chame **StgOpenStorage** para abrir o objeto OLE e retornar um objeto de armazenamento. 
      
   3. Chame o armazenamento retornado método do objeto **IStorage::CopyTo** para copiar para o objeto de armazenamento retornado da **OpenProperty**.
      
   4. Chame o método de **IStorage::Commit** do novo objeto de armazenamento. 
    
## <a name="set-prattachpathname"></a>Definir PR_ATTACH_PATHNAME
  
1. Aloca uma estrutura [SPropValue](spropvalue.md) , definindo o membro **ulPropTag** como **PR_ATTACH_PATHNAME** e o membro **Value.LPSZ** à cadeia de caracteres que representa o nome do arquivo. 
    
2. Chame o método de [IMAPIProp::SetProps](imapiprop-setprops.md) do anexo. 
    
> [!NOTE]
> Se sua plataforma suporta nomes extensos de arquivos, defina **PR_ATTACH_PATHNAME** e o **PR_ATTACH_LONG_PATHNAME**. Talvez seja necessário fazer com que um sistema operacional chamada para recuperar o nome de arquivo curto. 
  
## <a name="see-also"></a>Confira também

- [Anexos de MAPI](mapi-attachments.md)

