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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332939"
---
# <a name="creating-a-message-attachment"></a>Criar um anexo de mensagem
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um anexo de mensagem é de alguns dados adicionais, como um arquivo, outra mensagem ou um objeto OLE, que você pode enviar ou salvar junto com uma mensagem. Cada anexo tem uma coleção de propriedades que o identifica e descreve seu tipo e como ele é renderizado. Como destinatários, os anexos de mensagens só podem ser acessados por meio da mensagem à qual pertencem. Portanto, para que um anexo possa ser usado, sua mensagem deve estar aberta.
  
## <a name="create-a-message-attachment"></a>Criar um anexo de mensagem
  
1. Chame o método [IMessage:: CreateAttach](imessage-createattach.md) da mensagem e passe nulo como o identificador de interface. **CreateAttach** retorna um número que identifica exclusivamente o novo anexo dentro da mensagem. O número do anexo é armazenado na propriedade **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) e só é válido, desde que a mensagem que contém o anexo esteja aberta.
    
2. Chame [IMAPIProp::](imapiprop-setprops.md) SetProps para definir **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) para indicar como acessar o anexo. **PR_ATTACH_METHOD** é necessário. Defina-o como: 
    
   - ATTACH_BY_VALUE se o anexo for de dados binários.
    
   - ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE ou ATTACH_BY_REF_ONLY se o anexo for um arquivo.
    
   - ATTACH_EMBEDDED_MSG se o anexo for uma mensagem.
    
   - ATTACH_OLE se o anexo for um objeto OLE.
    
3. Defina a propriedade de dados de anexo apropriada:
    
   - **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) para dados binários e objetos OLE 1.
    
   - **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) para arquivos.
    
   - **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) para mensagens e objetos OLE 2.
    
4. Defina **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) para manter a representação gráfica do anexo para anexos de arquivo ou binário. Não o defina para objetos OLE, que armazenam as informações de renderização internamente ou para mensagens anexadas. 
    
5. Defina **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) para indicar onde o anexo deve ser exibido. **PR_RENDERING_POSITION** aplica-se somente aos clientes que definem a propriedade **PR_BODY** . Se você só oferecer suporte a **PR_RTF_COMPRESSED**, coloque as seguintes informações de espaço reservado no fluxo compactado:
    
   `\objattph`

   Para definir **PR_RENDERING_POSITION**, atribua um número que represente um deslocamento ordinal em caracteres, com o primeiro caractere de **PR_BODY** como 0, se você precisar saber onde na mensagem o anexo é renderizado, ou 0xFFFFFFFF, se você não renderizar anexos no **PR_BODY**.
    
6. Set **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) para indicar o nome curto do arquivo para um anexo de arquivo e **PR\_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) para indicar o nome do arquivo como suportado em uma plataforma que manipula o formato de nome de arquivo longo. Ambas as propriedades são opcionais. No enTanto, se você definir **PR_ATTACH_LONG_FILENAME**, defina também **PR_ATTACH_FILENAME**. 
    
7. Defina **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) para indicar o nome do anexo que pode aparecer em uma caixa de diálogo. PR_DISPLAY_NAME é opcional. 
    
## <a name="set-prattachdatabin"></a>Definir PR_ATTACH_DATA_BIN
  
1. Chame [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) para abrir a propriedade com a interface **IStream** . 
    
2. Se um arquivo contiver os dados e estiver aberto ou se você precisar de controle explícito sobre o tamanho do buffer, chame **IStream:: Write** em um loop para colocar os dados no Stream. 
    
3. Outra opção é chamar o **OpenStreamOnFile** para criar um fluxo para acessar o arquivo de dados e, em seguida, chamar o método **IStream:: CopyTo** do fluxo para copiar os dados para **** o Stream retornado por OpenProperty.
    
4. Chame o método **IStream:: Commit** do novo fluxo. 
    
## <a name="set-prattachdataobj"></a>Definir PR_ATTACH_DATA_OBJ
  
1. Chame **IMAPIProp:: OpenProperty** para abrir a propriedade com a interface **IStreamDocfile** para criar um fluxo que funcione com armazenamento estruturado. O **IStreamDocfile** é implementado por provedores de repositórios de mensagens para fornecer aos clientes uma maneira de maior desempenho para armazenar e recuperar o armazenamento estruturado. A interface **IStreamDocfile** é igual a **IStream**, mas é garantido que o conteúdo do Stream seja formatado como armazenamento estruturado. Se essa chamada for bem-sucedida, crie o Stream com as mesmas etapas descritas para a definição de **PR_ATTACH_DATA_BIN**.
    
2. Se **OpenProperty** falhar: 
    
   1. Chame **OpenProperty** novamente solicitando **IStorage**. 
      
   2. Chame **StgOpenStorage** para abrir o objeto OLE e retornar um objeto Storage. 
      
   3. Chame o método **IStorage:: CopyTo** do objeto de armazenamento retornado a ser copiado para o objeto **** de armazenamento retornado de OpenProperty.
      
   4. Chame o método **IStorage:: Commit** do novo objeto de armazenamento. 
    
## <a name="set-prattachpathname"></a>Definir PR_ATTACH_PATHNAME
  
1. Aloque uma estrutura [SPropValue](spropvalue.md) , definindo o membro **ulPropTag** como **PR_ATTACH_PATHNAME** e o membro **Value. lpsz** para a cadeia de caracteres que representa o nome do arquivo. 
    
2. Chame o método [IMAPIProp::](imapiprop-setprops.md) SetProps do anexo. 
    
> [!NOTE]
> Se sua plataforma suportar nomes de filelong, defina **PR_ATTACH_PATHNAME** e **PR_ATTACH_LONG_PATHNAME**. Talvez seja necessário fazer uma chamada do sistema operacional para recuperar o nome de arquivo curto. 
  
## <a name="see-also"></a>Confira também

- [Anexos MAPI](mapi-attachments.md)

