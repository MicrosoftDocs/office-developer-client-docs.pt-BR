---
title: Instalar os exemplos usados nesta seção
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 810f54bf-5b78-46b8-a617-4f61ff816400
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 288ece7a26fb89fa240339da681f163909124823
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397055"
---
# <a name="install-the-samples-used-in-this-section"></a>Instalar os exemplos usados nesta seção

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para instalar o aplicativo de MFCMAPI e o project CreateOutlookItemsAddin para exibir e executar o código de amostra referenciado pelos tópicos na seção [Criando itens do Outlook usando MAPI](creating-outlook-items-by-using-mapi.md) , siga estas etapas. 

Baixar e instalar exemplos usados no "usando MAPI para criar itens do Outlook" seção, siga estas etapas.

### <a name="to-download-and-install-the-mfcmapi-application-and-open-createoutlookitemsaddin-project"></a>Baixar e instalar o aplicativo MFCMAPI e abrir projeto CreateOutlookItemsAddin

1. Baixe a versão atual do [MFCMAPI](https://go.microsoft.com/fwlink/?LinkID=124154) executável para uma pasta no seu sistema. 
    
2. Extraia o arquivo MFCMapi.exe em MFCMapi.exe. _versão_zip para uma pasta vazia no disco rígido.
    
3. Baixe a versão atual do projeto [CreateOutlookItemsAddin](https://go.microsoft.com/fwlink/?LinkID=127828) . 
    
4. Extrai todos os arquivos no arquivo CreateOutlookItemsAddin.zip para a pasta onde você extraiu o arquivo MFCMapi.exe na etapa 2.
    
5. Copie MFCMapi.exe da pasta usada na etapa 2 para o diretório de compilação do projeto CreateOutlookItemsAddin (\CreateOutlookItemsAddin\Debug).
    
6. Abra o projeto CreateOutlookItemsAddin (\CreateOutlookItemsAddin\CreateOutlookItemsAddin.vcproj) no Visual Studio para examinar o código-fonte. Consulte os tópicos da seção [Criando itens do Outlook usando MAPI](creating-outlook-items-by-using-mapi.md) para determinar qual a fonte de arquivos para abrir. 
    
## <a name="run-mfcmapi-and-the-createoutlookitemsaddin-project"></a>Execute MFCMAPI e o projeto CreateOutlookItemsAddin

As etapas a seguir pressupõem que você tenha baixado e instalado a versão atual do executável MFCMAPI e o projeto CreateOutlookItemsAddin, conforme descrito no procedimento anterior. Estas etapas vão orientá-lo aos itens de menu **Addins** que permitem a criação de itens do Outlook usando o aplicativo de MFCMAPI e o projeto CreateOutlookItemsAddin. 
  
> [!NOTE]
> A pasta selecionada na etapa 8 e o comando que você seleciona na etapa 9, depende do tipo de item abordado em um destes tópicos da seção [Criando itens do Outlook usando MAPI](creating-outlook-items-by-using-mapi.md) . 

### <a name="to-run-the-mfcmapi-application-and-addins-menu-commands"></a>Para executar o aplicativo MFCMAPI e comandos do menu Addins

1. Inicie Mfcmapi.exe na pasta CreateOutlookItemsAddin\Debug que é criada quando você segue as instruções de instalação.
    
2. Clique em **Okey** para descartar a tela inicial do MFCMAPI. 
    
3. No menu de **sessão** , clique em **Logon e a tabela de repositório de exibição**.
    
4. Na caixa de diálogo **Escolher perfil** , selecione o perfil correto e clique em **Okey**. 
    
5. Clique duas vezes em **caixa de correio - _[Nome do usuário]_ ** na exibição de lista de tabela de repositório. 
    
6. Na exibição de árvore de pasta, expanda o nó raiz. O nome exibido para o nó raiz varia dependendo do tipo de perfil selecionado. Normalmente, esse nó é exibido como **raiz - caixa de correio**.
    
7. Na exibição de árvore de pasta, expanda o nó que contém o repositório de informações. O nome exibido para esse nó varia dependendo do tipo de perfil selecionado. Geralmente esse nó é exibido como **IPM_SUBTREE** ou **Superior do armazenamento de informações**.
    
8. Clique duas vezes na pasta para o tipo de item criar. Por exemplo, para criar um compromisso, clique na pasta de **compromissos** . 
    
9. No menu **Addins** , clique no comando apropriado para o item criar. 
    
## <a name="download-and-view-code-from-the-mfcmapi-application"></a>Baixe e exiba o código do aplicativo MFCMAPI

Alguns tópicos referem-se ao código-fonte do próprio aplicativo MFCMAPI. As etapas a seguir descrevem como baixar o código-fonte MFCMAPI e exibi-lo no Visual Studio. 

### <a name="to-download-and-view-the-mfcmapi-application-source-code"></a>Fazer o download e ler o código-fonte MFCMAPI aplicativo

1. Baixe o código-fonte para a versão atual do aplicativo [MFCMAPI](https://go.microsoft.com/fwlink/?LinkID=124154) para uma pasta no seu sistema. 
    
2. Extraia os arquivos no MFCMAPI - zip de _conjunto de alterações_para uma pasta vazia no disco rígido.
    
3. Abra o projeto MFCMapi (\ _nomedapasta_\ MFCMapi.vcproj) no Visual Studio para examinar o código-fonte.
    
## <a name="see-also"></a>Confira também

- [Criar um Item de email simples](how-to-create-a-simple-mail-item.md)
- [Criar um Item de tarefa recorrente simples](how-to-create-a-simple-recurrent-task-item.md)
- [Criar um Item de compromisso recorrente complexa](how-to-create-a-complex-recurrent-appointment-item.md)
- [Leia e analisar um padrão de recorrência](how-to-read-and-parse-a-recurrence-pattern.md)

