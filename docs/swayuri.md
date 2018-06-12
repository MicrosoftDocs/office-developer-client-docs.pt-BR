---
title: SwayURI
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 11daa75b-87fc-4e63-8e02-09ab9307c8f8
ms.date: 01/28/2016
description: Use o esquema de URI Sway para abrir o aplicativo Sway e exibir ou editar um Sway.
ms.openlocfilehash: 7a820339abcd666e7e1b9ad584cd152ca8fd4f68
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771245"
---
# <a name="sway-uri-scheme"></a>Esquema de URI de sway

Este documento define o formato do Uniform Resource Identifiers (URIs) para o aplicativo Sway para Windows. Você pode usar o esquema de URI para invocar o aplicativo Sway com diversos comandos.

## <a name="sway-uri-scheme-syntax"></a>Sintaxe do esquema de URI de sway

A sintaxe do esquema URI veja a seguir:

`<ms-sway>:<command-argument>`

- `<ms-sway>`&ndash; Indica que o Sway é o aplicativo para chamar. Quando Sway para Windows é instalado, `ms-sway` está registrado com o Windows para ser o manipulador Sway.
- `<command-argument>`&ndash; Uma URI pode ter um ou mais argumentos de comando, delimitados pelo e comercial (`&`) caracteres. Quando mais de um argumento de comando está incluído em um URI, um e comercial (`&`) caractere deve separar cada argumento de comando do argumento de comando a seguir. Argumentos de comando variam de acordo com o cenário. 

## <a name="command-arguments"></a>Argumentos de comando

Vários argumentos de comando podem ser incluídos como parte do esquema de URL Sway. Desses argumentos de comando não são necessários. Se você não incluir os argumentos de comando, o aplicativo Sway é invocado.

|Nome de argumento do comando|Descrição|Tipo|Valores possíveis|Necessário?|
|:-----|:-----|:-----|:-----|:-----|
|
  **id**|O identificador exclusivo de um Sway. Usado para indicar o Sway a serem abertas.|Cadeia de caracteres|Um identificador exclusivo válido para um Sway. A identificação sempre é parte da URL para um Sway.<br/><br/>Por exemplo, para o seguinte Sway `https://sway.com/dBheQgVZ1RQBfiQU`, a id é `dBheQgVZ1RQBfiQU`.<br/><br/>Se a conta de usuário associada ao aplicativo Sway tiver permissões de edição, o aplicativo abre o Sway no modo de edição. Caso contrário, o aplicativo abre o Sway no modo de exibição.|Não|
|**modo**|O modo no qual um Sway específica deve ser aberta, para edição ou para exibição.|Cadeia de caracteres|edit<br/>modo de exibição<br/><br/>**Observação**: se nenhuma **identificação** for especificado, esse argumento do comando será ignorado.|Não|
|**auth_upn**|A conta a ser usado ao abrir Sway.|Cadeia de caracteres|Um endereço de email válido.<br/><br/>Se o endereço de email especificado não estiver associado uma conta de Sway, Sway pede ao usuário entrar como o usuário especificado.<br/><br/>Se mais de uma conta está associada ao aplicativo Sway e o endereço de email especificado existe, o aplicativo Sway alterna para usando essa conta quando invocado.|Não|
|**autenticação\_pvr**|O tipo de conta a ser usada para abrir o Sway&mdash;uma conta Microsoft ou uma conta do Windows Azure Active Directory (AD Azure).|Cadeia de caracteres|WindowsLiveId – Especifica que o **auth\_upn** é uma conta da Microsoft.<br/><br/>OrgId – Especifica que o **auth\_upn** conta é uma conta do Windows Azure AD.<br/><br/>Se nenhum **auth\_upn** for especificado, esse argumento do comando é ignorado.|Não|
|**invocação\_app**|O nome do aplicativo Windows utilizado para chamar Sway.|Cadeia de caracteres|O nome amigável do aplicativo Windows utilizado para chamar Sway via o esquema de URL Sway.<br/><br/>A finalidade deste argumento do comando é de telemetria e acompanhamento.|Não|

## <a name="uri-scheme-semantics"></a>Semântica de esquema URI

O `<ms-sway>` esquema define uma sintaxe URI para abrir um Sway ou para o aplicativo Sway de invocação. O esquema define vários argumentos de comando, que podem ser usados para fazer o seguinte: 

- Abra o aplicativo Sway &ndash; nenhum argumento do comando precisa ser especificado. 

- Abrir um Sway para exibição no aplicativo Sway &ndash; a **id** e o **modo** definido para exibir precisam ser especificado. 

- Abra um Sway para edição no aplicativo Sway &ndash; a **id** e o **modo** definido como para editar precisam ser especificados. Recomendamos que você inclua também **auth\_upn** e **auth\_pvr** para ajudar a garantir que a conta correta com permissões de edição é usada quando Sway é aberto.  

## <a name="example"></a>Example

`ms-sway:id=CyrvEYLmFKi1B2_I&auth_upn=account@email.com&auth_pvr=WindowsLiveId&invoking_app=MyApp` 


