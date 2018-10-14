---
title: Suporte do Office para Android para a Estrutura de Acesso ao Armazenamento do Android
manager: soliver
ms.date: 06/18/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9cfed295-f499-44dc-bac5-9e266df1b5b3
description: O Office para Android se integra à Estrutura de Acesso ao Armazenamento do Android, que permite ao Office abrir arquivos armazenados por outro provedor de documentos.
ms.openlocfilehash: 24d7e48106aeb5e58a668b94cbde00eaa9175230
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384546"
---
# <a name="office-for-android-support-for-the-android-storage-access-framework"></a>Suporte do Office para Android para a Estrutura de Acesso ao Armazenamento do Android

O Office para Android se integra à Estrutura de Acesso ao Armazenamento do Android, que permite ao Office abrir arquivos armazenados por outro provedor de documentos.
  
O Android 4.4 (API nível 19) é o primeiro a incluir a Estrutura de Acesso ao Armazenamento (SAF). A SAF permite aos usuários navegar e abrir documentos, imagens e outros arquivos em todos os seus provedores de armazenamento de documento favoritos. Uma interface de usuário padrão permite aos usuários procurar arquivos e acessá-los de forma consistente entre aplicativos e provedores.
  
## <a name="implement-a-document-provider"></a>Implementar um provedor de documento

Se você estiver desenvolvendo um aplicativo que fornece serviços de armazenamento para documentos, você pode disponibilizar arquivos por SAF [escrevendo um provedor de documentos personalizado](https://developer.android.com/guide/topics/providers/document-provider.html). Os aplicativos do Office poderão então usar a finalidade [ACTION_OPEN_DOCUMENT](https://developer.android.com/reference/android/content/Intent.html) e/ou [ACTION_CREATE_DOCUMENT](https://developer.android.com/reference/android/content/Intent.html) para receber os arquivos retornados ao seu provedor de documentos. Observe que a finalidade pode conter filtros para refinar ainda mais os critérios. 
  
## <a name="enable-free-consumer-edits"></a>Ativar edições de consumidor gratuito

Os usuários podem entrar em aplicativos do Office com uma conta gratuita da Microsoft para criar ou editar documentos armazenados em um serviço de armazenamento direcionado ao consumidor. A tabela a seguir lista as propriedades obrigatórias que os provedores deverão fornecer como parte do cursor para habilitar a edição gratuita do consumidor para documentos acessados por meio da Estrutura de Acesso ao Armazenamento.
  
|**Propriedade**|**Índice**|**Valor**|
|:-----|:-----|:-----|
|Tipo de Documento  <br/> |com_microsoft_office_doctype  <br/> |\<consumidor\>  <br/> |
|Nome amigável do dispositivo  <br/> |com_microsoft_office_servicename  <br/> |Qualquer nome amigável para o serviço usado para identificar um documento na lista Recentes nos aplicativos do Office. Observe que a propriedade "Contrato de termos de uso" deve ser fornecida antes do nome amigável para o serviço poder ser exibido.  <br/> |
|Acordos de termos de uso  <br/> |com_microsoft_office_termsofuse  <br/> |\<Eu concordo com os termos localizados em https://go.microsoft.com/fwlink/p/?LinkId=528381\>  <br/> |
   
## <a name="see-also"></a>Confira também
<a name="bk_addresources"> </a>

- [Integração com o Office](integrate-with-office.md)
    
- [Noções básicas sobre provedores de conteúdo](hhttps://developer.android.com/guide/topics/providers/content-provider-basics.html)
    
- [Criar um provedor de conteúdo](https://developer.android.com/guide/topics/providers/content-provider-creating.html)
    
- [Guia para desenvolvedores da Estrutura de Acesso ao Armazenamento](https://developer.android.com/guide/topics/providers/document-provider.html)
    

