---
title: SwayURI
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 11daa75b-87fc-4e63-8e02-09ab9307c8f8
ms.date: 01/28/2016
description: Use o esquema URI de Sway para abrir o aplicativo Sway e exibir ou editar um Sway.
ms.openlocfilehash: 04848ef1de2777d916d8dd8dd381e6d5f66310d6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415310"
---
# <a name="sway-uri-scheme"></a>Esquema do URI do Sway

Este documento define o formato de URI (Uniform Resource Identifiers) para o aplicativo Sway para Windows. Você pode usar esse esquema URI para invocar o aplicativo Sway com vários comandos.

## <a name="sway-uri-scheme-syntax"></a>Sintaxe do esquema URI do Sway

Veja a seguir a sintaxe do esquema URI:

`<ms-sway>:<command-argument>`

- `<ms-sway>`&ndash; Indica que o Sway é o aplicativo a ser chamado. Quando o Sway para Windows é instalado `ms-sway` , ele é registrado com o Windows para ser o manipulador de Sway.
- `<command-argument>`&ndash; Um URI pode ter um ou mais argumentos de comando, delimitados pelo caractere`&`e comercial (). Quando mais de um argumento de comando é incluído em um URI, um caractere`&`de e comercial () deve separar cada argumento de comando do argumento de comando a seguir. Os argumentos de comando variam de acordo com o cenário. 

## <a name="command-arguments"></a>Argumentos de comando

Vários argumentos de comando podem ser incluídos como parte do esquema de URL do Sway. Estes argumentos de comando não são necessários. Se você não incluir os argumentos do comando, o aplicativo Sway será invocado.

|Nome do argumento do comando|Descrição|Tipo|Valores possíveis|Obrigatório?|
|:-----|:-----|:-----|:-----|:-----|
|**id**|O identificador exclusivo de um Sway. Usado para indicar que o Sway deve ser aberto.|String|Um identificador exclusivo válido para um Sway. A ID é sempre parte da URL para um Sway.<br/><br/>Por exemplo, para o seguinte Sway `https://sway.com/dBheQgVZ1RQBfiQU`, a ID é `dBheQgVZ1RQBfiQU`.<br/><br/>Se a conta de usuário associada ao aplicativo Sway tiver permissões editar, o aplicativo abrirá o Sway no modo de edição. Caso contrário, o aplicativo abrirá o Sway no modo de exibição.|Não|
|**modo**|O modo no qual um Sway específico deve ser aberto, seja para edição ou para exibição.|String|edit<br/>modo de exibição<br/><br/>**Observação**: se nenhuma **ID** for especificada, este argumento de comando será ignorado.|Não|
|**auth_upn**|A conta a ser usada ao abrir Sway.|String|Um endereço de email válido.<br/><br/>Se o endereço de email especificado não estiver associado a uma conta de Sway, o Sway solicitará que o usuário entre como o usuário especificado.<br/><br/>Se mais de uma conta estiver associada ao aplicativo Sway e o endereço de email especificado existir, o aplicativo Sway alterna para usar essa conta quando invocada.|Não|
|**PVR\_de autenticação**|O tipo de conta a ser usado para abrir o&mdash;Sway como uma conta da Microsoft ou uma conta do Azure Active Directory (Azure AD).|String|WindowsLiveId – especifica que a **conta\_UPN de autenticação** é uma conta da Microsoft.<br/><br/>OrgId – especifica que a conta de **UPN de autenticação\_** é uma conta do Azure AD.<br/><br/>Se nenhum **UPN\_de autenticação** for especificado, este argumento de comando será ignorado.|Não|
|**invocando\_aplicativo**|O nome do aplicativo do Windows usado para invocar o Sway.|String|O nome amigável do aplicativo do Windows usado para invocar o Sway por meio do esquema de URL do Sway.<br/><br/>O objetivo desse argumento de comando é para telemetria e controle.|Não|

## <a name="uri-scheme-semantics"></a>Semântica do esquema URI

O `<ms-sway>` esquema define uma sintaxe de URI para abrir um Sway ou para invocar o aplicativo Sway. O esquema define vários argumentos de comando, que podem ser usados para fazer o seguinte: 

- Abrir o aplicativo &ndash; Sway nenhum argumento de comando precisa ser especificado. 

- Abrir um Sway para exibição no aplicativo &ndash; Sway a **ID** e o **modo** definidos para o modo de exibição precisam ser especificados. 

- Abrir um Sway para edição no aplicativo &ndash; Sway a **ID** e o **modo** definido para edição precisam ser especificados. Recomendamos que você também inclua **o\_UPN de autenticação** e o **PVR de autenticação\_** para ajudar a garantir que a conta correta com permissões de edição seja usada quando o Sway for aberto.  

## <a name="example"></a>Exemplo

`ms-sway:id=CyrvEYLmFKi1B2_I&auth_upn=account@email.com&auth_pvr=WindowsLiveId&invoking_app=MyApp` 


