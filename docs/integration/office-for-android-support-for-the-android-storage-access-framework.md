---
title: Suporte do Office para Android para a Estrutura de acesso ao armazenamento do Android
manager: soliver
ms.date: 06/18/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9cfed295-f499-44dc-bac5-9e266df1b5b3
description: Office para Android integra-se a estrutura de acesso do armazenamento Android, que permite ao Office abrir arquivos armazenados pelo provedor de outro documento.
ms.openlocfilehash: c217eb2aa6c0974c32e60f5015449de7b157d39d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765763"
---
# <a name="office-for-android-support-for-the-android-storage-access-framework"></a>Suporte do Office para Android para a Estrutura de acesso ao armazenamento do Android

Office para Android integra-se a estrutura de acesso do armazenamento Android, que permite ao Office abrir arquivos armazenados pelo provedor de outro documento.
  
Android 4.4 (nível de API 19) apresenta a estrutura de acesso de armazenamento (SAF). O SAF permite que os usuários procurem e abrir documentos, imagens e outros arquivos entre todos os seus provedores de armazenamento de documento preferencial. Uma interface de usuário padrão permite aos usuários navegar por arquivos e acessá-las de forma consistente entre provedores e aplicativos.
  
## <a name="implement-a-document-provider"></a>Implementar um provedor de documento

Se você estiver desenvolvendo um aplicativo que fornece serviços de armazenamento de documentos, você pode fazer com que seus arquivos disponíveis por meio do SAF ao [escrever um provedor de documento personalizadas](https://developer.android.com/guide/topics/providers/document-provider.html). Aplicativos do Office podem então chamar a intenção [ACTION_OPEN_DOCUMENT](https://developer.android.com/reference/android/content/Intent.html) e/ou [ACTION_CREATE_DOCUMENT](https://developer.android.com/reference/android/content/Intent.html) para receber os arquivos retornados pelo seu provedor de documento. Observe que a intenção pode incluir filtros para refinar os critérios. 
  
## <a name="enable-free-consumer-edits"></a>Habilitar edições do consumidor gratuito

Os usuários podem se conectar ao Office apps com uma conta da Microsoft gratuito para criar ou editar documentos armazenados em um serviço de armazenamento orientado ao consumidor. A tabela a seguir lista as propriedades obrigatórias que provedores deverá fornecer como parte do cursor, para ativar a edição de consumidor gratuito para documentos acessados por meio da estrutura de acesso de armazenamento.
  
|**Propriedade**|**Index**|**Valor**|
|:-----|:-----|:-----|
|Tipo de documento  <br/> |com_microsoft_office_doctype  <br/> |\<consumidor\>  <br/> |
|Nome amigável do serviço  <br/> |com_microsoft_office_servicename  <br/> |Qualquer nome amigável para o serviço, usado para identificar um documento na lista recente no Office apps. Observe que a propriedade "Termos do contrato de uso" deve ser fornecida antes do nome amigável para o serviço pode ser exibido.  <br/> |
|Termos do contrato de uso  <br/> |com_microsoft_office_termsofuse  <br/> |\<Eu concordar com os termos localizados emhttp://go.microsoft.com/fwlink/p/?LinkId=528381\>  <br/> |
   
## <a name="see-also"></a>Confira também
<a name="bk_addresources"> </a>

- [Integração com o Office](integrate-with-office.md)
    
- [Noções básicas do provedor de conteúdo](hhttps://developer.android.com/guide/topics/providers/content-provider-basics.html)
    
- [Criando um provedor de conteúdo](https://developer.android.com/guide/topics/providers/content-provider-creating.html)
    
- [Guia do desenvolvedor do armazenamento Access Framework](https://developer.android.com/guide/topics/providers/document-provider.html)
    

