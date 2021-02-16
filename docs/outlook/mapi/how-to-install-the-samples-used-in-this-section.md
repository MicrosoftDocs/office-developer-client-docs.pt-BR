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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345546"
---
# <a name="install-the-samples-used-in-this-section"></a>Instalar os exemplos usados nesta seção

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para instalar o aplicativo MFCMAPI e o projeto CreateOutlookItemsAddin para exibir e executar o código de exemplo referenciado pelos tópicos na seção Criando itens do Outlook usando [MAPI,](creating-outlook-items-by-using-mapi.md) siga estas etapas. 

Para baixar e instalar os exemplos usados na seção "Usando MAPI para criar itens do Outlook", siga estas etapas.

### <a name="to-download-and-install-the-mfcmapi-application-and-open-createoutlookitemsaddin-project"></a>Para baixar e instalar o aplicativo MFCMAPI e abrir o projeto CreateOutlookItemsAddin

1. Baixe a versão atual do [executável MFCMAPI](https://go.microsoft.com/fwlink/?LinkID=124154) para uma pasta em seu sistema. 
    
2. Extraia MFCMapi.exe arquivo de MFCMapi.exe. _version_.zip to an empty folder on your hard drive.
    
3. Baixe a versão atual do [projeto CreateOutlookItemsAddin.](https://go.microsoft.com/fwlink/?LinkID=127828) 
    
4. Extraia todos os arquivos CreateOutlookItemsAddin.zip arquivo para a pasta onde você extraiu o arquivo MFCMapi.exe na Etapa 2.
    
5. Copie MFCMapi.exe da pasta usada na Etapa 2 para o diretório de com build do projeto CreateOutlookItemsAddin (\CreateOutlookItemsAddin\Debug).
    
6. Abra o projeto CreateOutlookItemsAddin (\CreateOutlookItemsAddin\CreateOutlookItemsAddin.vcproj) no Visual Studio para examinar o código-fonte. Consulte os tópicos da seção Criando itens do [Outlook usando MAPI](creating-outlook-items-by-using-mapi.md) para determinar quais arquivos de origem serão abertos. 
    
## <a name="run-mfcmapi-and-the-createoutlookitemsaddin-project"></a>Executar MFCMAPI e o projeto CreateOutlookItemsAddin

As etapas a seguir presumem que você tenha baixado e instalado a versão atual do executável MFCMAPI e do projeto CreateOutlookItemsAddin conforme descrito no procedimento anterior. Estas etapas orientarão você para os itens de menu **Addins** que permitem criar itens do Outlook usando o aplicativo MFCMAPI e o projeto CreateOutlookItemsAddin. 
  
> [!NOTE]
> A pasta selecionada na etapa 8 e o comando selecionado na etapa 9 dependem do tipo de item discutido em um dos tópicos da seção Criando itens do Outlook usando [MAPI.](creating-outlook-items-by-using-mapi.md) 

### <a name="to-run-the-mfcmapi-application-and-addins-menu-commands"></a>Para executar os comandos do aplicativo MFCMAPI e do menu Addins

1. Inicie Mfcmapi.exe na pasta CreateOutlookItemsAddin\Debug que é criada quando você segue as instruções de instalação.
    
2. Clique **em OK** para descartar a tela inicial MFCMAPI. 
    
3. No menu **Sessão,** clique em **Logon e Exibir Tabela do Store.**
    
4. Na caixa **de diálogo Escolher** Perfil, selecione o perfil correto e clique em **OK.** 
    
5. Clique duas vezes **em Caixa de Correio – _[Nome de Usuário]_** na exibição de lista da tabela da loja. 
    
6. Na exibição de árvore de pastas, expanda o nó raiz. O nome exibido para o nó raiz varia dependendo do tipo de perfil selecionado. Normalmente, esse nó é exibido como **Raiz - Caixa de Correio.**
    
7. Na exibição de árvore de pastas, expanda o nó que contém o armazenamento de informações. O nome exibido para esse nó varia dependendo do tipo de perfil selecionado. Normalmente, esse nó é exibido como **IPM_SUBTREE** ou Início do Armazenamento **de Informações.**
    
8. Clique duas vezes na pasta para o tipo de item a ser criado. Por exemplo, para criar um compromisso, clique na **pasta Compromissos.** 
    
9. No menu **Addins,** clique no comando apropriado para o item a ser criado. 
    
## <a name="download-and-view-code-from-the-mfcmapi-application"></a>Baixar e exibir o código do aplicativo MFCMAPI

Alguns tópicos se referem ao código-fonte do próprio aplicativo MFCMAPI. As etapas a seguir descrevem como baixar o código-fonte MFCMAPI e exibi-lo no Visual Studio. 

### <a name="to-download-and-view-the-mfcmapi-application-source-code"></a>Para baixar e exibir o código-fonte do aplicativo MFCMAPI

1. Baixe o código-fonte da versão atual do [aplicativo MFCMAPI](https://go.microsoft.com/fwlink/?LinkID=124154) para uma pasta em seu sistema. 
    
2. Extraia os arquivos em MFCMAPI - _changeset_.zip para uma pasta vazia no disco rígido.
    
3. Abra o projeto MFCMapi (\ _foldername_\ MFCMapi.vcproj) no Visual Studio para examinar o código-fonte.
    
## <a name="see-also"></a>Confira também

- [Criar um Item de Email Simples](how-to-create-a-simple-mail-item.md)
- [Criar um item de tarefa recorrente simples](how-to-create-a-simple-recurrent-task-item.md)
- [Criar um item de compromisso recorrente complexo](how-to-create-a-complex-recurrent-appointment-item.md)
- [Ler e analisar um padrão de recorrência](how-to-read-and-parse-a-recurrence-pattern.md)

