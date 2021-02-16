---
title: SwayURI
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 11daa75b-87fc-4e63-8e02-09ab9307c8f8
ms.date: 01/28/2016
description: Use o esquema de URI do Sway para abrir o aplicativo Sway e exibir ou editar um Sway.
ms.openlocfilehash: 04848ef1de2777d916d8dd8dd381e6d5f66310d6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415310"
---
# <a name="sway-uri-scheme"></a>Esquema do URI do Sway

Este documento define o formato de URIs (Uniform Resource Identifiers) para o aplicativo Sway para Windows. Você pode usar esse esquema de URI para invocar o aplicativo Sway com vários comandos.

## <a name="sway-uri-scheme-syntax"></a>Sintaxe do esquema de URI do Sway

A seguir está a sintaxe do esquema de URI:

`<ms-sway>:<command-argument>`

- `<ms-sway>`&ndash;Indica que o Sway é o aplicativo a ser invocado. Quando o Sway para Windows está instalado, `ms-sway` é registrado no Windows para ser o manipulador do Sway.
- `<command-argument>`Um URI pode ter um ou mais argumentos de comando, delimitados pelo &ndash; caractere E ampersand ( `&` ). Quando mais de um argumento de comando é incluído em um URI, um caractere ESame () deve separar cada argumento de comando do argumento de comando a `&` seguir. Os argumentos de comando variam de acordo com o cenário. 

## <a name="command-arguments"></a>Argumentos de comando

Vários argumentos de comando podem ser incluídos como parte do esquema de URL do Sway. Esses argumentos de comando não são necessários. Se você não incluir os argumentos de comando, o aplicativo Sway será invocado.

|Nome do argumento de comando|Descrição|Tipo|Valores possíveis|Obrigatório?|
|:-----|:-----|:-----|:-----|:-----|
|**id**|O identificador exclusivo de um Sway. Usado para indicar o Sway a ser aberto.|String|Um identificador exclusivo válido para um Sway. A id sempre faz parte da URL para um Sway.<br/><br/>Por exemplo, para o Sway a `https://sway.com/dBheQgVZ1RQBfiQU` seguir, a id é `dBheQgVZ1RQBfiQU` .<br/><br/>Se a conta de usuário associada ao aplicativo Sway tiver permissões de edição, o aplicativo abrirá o Sway no modo de edição. Caso contrário, o aplicativo abre o Sway no modo de exibição.|Não|
|**modo**|O modo no qual um Sway específico deve ser aberto, seja para edição ou para exibição.|String|edit<br/>modo de exibição<br/><br/>**OBSERVAÇÃO:** se **nenhuma id** for especificada, esse argumento de comando será ignorado.|Não|
|**auth_upn**|A conta a ser usada ao abrir o Sway.|String|Um endereço de email válido.<br/><br/>Se o endereço de email especificado não estiver associado a uma conta do Sway, o Sway pedirá ao usuário para entrar como o usuário especificado.<br/><br/>Se mais de uma conta estiver associada ao aplicativo Sway e o endereço de email especificado existir, o aplicativo Sway alterna para usar essa conta quando invocado.|Não|
|**auth \_ pvr**|O tipo de conta a ser usada para abrir o Sway uma conta da Microsoft ou uma conta do &mdash; Azure Active Directory (Azure AD).|String|WindowsLiveId – Especifica que a conta de upn de **\_ auth** é uma conta da Microsoft.<br/><br/>OrgId – Especifica que a conta **de auth \_ upn** é uma conta do Azure AD.<br/><br/>Se nenhum **\_ upn de auth** for especificado, esse argumento de comando será ignorado.|Não|
|**invocando \_ aplicativo**|O nome do aplicativo do Windows usado para invocar o Sway.|String|O nome amigável do aplicativo do Windows usado para invocar o Sway por meio do esquema de URL do Sway.<br/><br/>O objetivo deste argumento de comando é telemetria e rastreamento.|Não|

## <a name="uri-scheme-semantics"></a>Semântica do esquema de URI

O esquema define uma sintaxe de URI para abrir um Sway ou para `<ms-sway>` invocar o aplicativo Sway. O esquema define vários argumentos de comando, que podem ser usados para fazer o seguinte: 

- Abra o aplicativo &ndash; Sway. Nenhum argumento de comando precisa ser especificado. 

- Abra um Sway para exibição no aplicativo Sway A id e o modo definidos para &ndash; exibição precisam ser especificados.   

- Abra um Sway para edição no aplicativo Sway A id e o modo definidos para &ndash; edição precisam ser especificados.   Recomendamos que você também inclua **auth \_ upn** e **\_ pvr** de autorização para ajudar a garantir que a conta certa com permissões de edição seja usada quando o Sway for aberto.  

## <a name="example"></a>Exemplo

`ms-sway:id=CyrvEYLmFKi1B2_I&auth_upn=account@email.com&auth_pvr=WindowsLiveId&invoking_app=MyApp` 


