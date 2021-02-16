---
title: Criar um anexo de mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 711b6765-7763-41ae-9ff8-61ca6ddd459d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2bdba3574c962c825f45cd098efa1cba6e21a4ea
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405993"
---
# <a name="creating-a-message-attachment"></a>Criar um anexo de mensagem
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um anexo de mensagem são alguns dados adicionais, como um arquivo, outra mensagem ou um objeto OLE, que você pode enviar ou salvar junto com uma mensagem. Cada anexo tem uma coleção de propriedades que o identifica e descreve seu tipo e como ele é renderizado. Assim como os destinatários, os anexos de mensagens só podem ser acessados por meio da mensagem à qual pertencem. Portanto, para que um anexo seja usável, sua mensagem deve estar aberta.
  
## <a name="create-a-message-attachment"></a>Criar um anexo de mensagem
  
1. Chame o método [IMessage::CreateAttach](imessage-createattach.md) da mensagem e passe NULL como o identificador da interface. **CreateAttach** retorna um número que identifica exclusivamente o novo anexo dentro da mensagem. O número do anexo é armazenado na propriedade **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) e é válido apenas enquanto a mensagem que contém o anexo está aberta.
    
2. Chame [IMAPIProp::SetProps](imapiprop-setprops.md) para definir **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) para indicar como acessar o anexo. **PR_ATTACH_METHOD** é necessário. De definida como: 
    
   - ATTACH_BY_VALUE se o anexo for dados binários.
    
   - ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE ou ATTACH_BY_REF_ONLY se o anexo for um arquivo.
    
   - ATTACH_EMBEDDED_MSG se o anexo for uma mensagem.
    
   - ATTACH_OLE se o anexo for um objeto OLE.
    
3. De definir a propriedade de dados de anexo apropriada:
    
   - **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) para dados binários e objetos OLE 1.
    
   - **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) para arquivos.
    
   - **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) para mensagens e objetos OLE 2.
    
4. De **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) para manter a representação gráfica do anexo para anexos de arquivo ou binários. Não a de definida para objetos OLE, que armazenam as informações de renderização internamente ou para mensagens anexadas. 
    
5. De **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) para indicar onde o anexo deve ser exibido. **PR_RENDERING_POSITION** aplica-se somente a clientes que definirem a **PR_BODY** propriedade. Se você só tiver **suporte PR_RTF_COMPRESSED**, coloque as seguintes informações de espaço reservado no fluxo compactado:
    
   `\objattph`

   Para definir **PR_RENDERING_POSITION**, atribua um número que representa um deslocamento ordinal em caracteres, com o primeiro caractere de **PR_BODY** sendo 0, se você precisar saber onde na mensagem o anexo é renderizado ou 0xFFFFFFFF, se você não renderizar anexos no **PR_BODY**.
    
6. Set **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) to indicate the short name of the file for a file attachment and **PR \_ ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) to indicate the name of the file as supported on a platform that handles the long filename format. Ambas as propriedades são opcionais. No entanto, se você definir **PR_ATTACH_LONG_FILENAME**, também definir **PR_ATTACH_FILENAME**. 
    
7. De **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) para indicar o nome do anexo que pode aparecer em uma caixa de diálogo. PR_DISPLAY_NAME é opcional. 
    
## <a name="set-pr_attach_data_bin"></a>Definir PR_ATTACH_DATA_BIN
  
1. Chame [IMAPIProp::OpenProperty](imapiprop-openproperty.md) para abrir a propriedade com a interface **IStream.** 
    
2. Se um arquivo contiver os dados e ele estiver aberto ou se você precisar de controle explícito sobre o tamanho do buffer, chame **IStream::Write** em um loop para colocar os dados no fluxo. 
    
3. Outra opção é chamar **OpenStreamOnFile** para criar um fluxo para acessar o arquivo de dados e, em seguida, chamar o método **IStream::CopyTo** desse fluxo para copiar os dados para o fluxo retornado por **OpenProperty**.
    
4. Chame o método **IStream::Commit** do novo fluxo. 
    
## <a name="set-pr_attach_data_obj"></a>Definir PR_ATTACH_DATA_OBJ
  
1. Chame **IMAPIProp::OpenProperty** para abrir a propriedade com a interface **IStreamDocfile** para criar um fluxo que funciona com armazenamento estruturado. **O IStreamDocfile é** implementado pelos provedores de armazenamento de mensagens para dar aos clientes uma maneira de alto desempenho de armazenar e recuperar o armazenamento estruturado. A interface **IStreamDocfile** é igual a **IStream**, mas o conteúdo do fluxo tem garantia de ser formatado como armazenamento estruturado. Se essa chamada for bem-sucedida, crie o fluxo com as mesmas etapas descritas para definir **PR_ATTACH_DATA_BIN**.
    
2. Se **OpenProperty** falhar: 
    
   1. Chame **OpenProperty** novamente solicitando **IStorage**. 
      
   2. Chame **StgOpenStorage** para abrir o objeto OLE e retornar um objeto de armazenamento. 
      
   3. Chame o método **IStorage::CopyTo** do objeto de armazenamento retornado para copiar para o objeto de armazenamento retornado de **OpenProperty**.
      
   4. Chame o método **IStorage::Commit do** novo objeto de armazenamento. 
    
## <a name="set-pr_attach_pathname"></a>Definir PR_ATTACH_PATHNAME
  
1. Aloce uma [estrutura SPropValue,](spropvalue.md) definindo o **membro ulPropTag** como **PR_ATTACH_PATHNAME** e o membro **Value.LPSZ** para a cadeia de caracteres que representa o nome de arquivo. 
    
2. Chame o método [IMAPIProp::SetProps do](imapiprop-setprops.md) anexo. 
    
> [!NOTE]
> Se sua plataforma oferece suporte a nomes de arquivo longos, **de** definida PR_ATTACH_PATHNAME e **PR_ATTACH_LONG_PATHNAME**. Pode ser necessário fazer uma chamada do sistema operacional para recuperar o nome de arquivo curto. 
  
## <a name="see-also"></a>Confira também

- [Anexos MAPI](mapi-attachments.md)

