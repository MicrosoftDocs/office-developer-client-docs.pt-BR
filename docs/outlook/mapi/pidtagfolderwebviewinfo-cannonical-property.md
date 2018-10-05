---
title: Propriedade canônica PidTagFolderWebViewInfo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFolderWebViewInfo
api_type:
- HeaderDef
ms.assetid: 96ea23df-aa4f-4b3e-9663-e7db39f668c1
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 70932e703511235e9f5e32efd95b18d1b66494e2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389957"
---
# <a name="pidtagfolderwebviewinfo-cannonical-property"></a>Propriedade canônica PidTagFolderWebViewInfo

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém a URL da home page de uma pasta no Microsoft Outlook. Essa propriedade contém um fluxo binário chamado **WebViewPersistenceObject**.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_FOLDER_WEBVIEWINFO  <br/> |
|Identificador:  <br/> |0x36DF  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Pasta MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Uma URL da home page pode ser especificada para qualquer pasta do Outlook. Essas informações podem ser acessadas no Outlook a partir da guia **página inicial** da caixa de diálogo Propriedades de uma pasta. 
  
Dependendo de determinadas configurações de diretiva, a home page pode ser ignorada pelo Outlook se o repositório MAPI que contém essa pasta não relata MSCAP_SECURE_FOLDER_HOMEPAGES em sua implementação [IMSCapabilities::GetCapabilities](pidtagfolderwebviewinfo-cannonical-property.md) . 
  
**A pasta** e uma pasta pública podem ter URLs de home page. No entanto **a pasta** usa um mecanismo diferente para gerenciar sua URL da home page; Esse mecanismo não é abordado neste tópico. Uma pasta pública também pode ter uma URL da home page definido dentro dela que é específico para um usuário. No entanto, esse recurso não está descrito neste tópico. 
  
O valor dessa propriedade é um fluxo binário chamado **WebViewPersistenceObject**.
  
### <a name="webviewpersistenceobject-stream-structure"></a>Estrutura de fluxo de WebViewPersistenceObject

A estrutura de fluxo de **WebViewPersistenceObject** contém informações sobre uma URL da home page de uma pasta. 
  
Elementos de dados nesta estrutura são armazenados na ordem de bytes pouca-endian, imediatamente após uns aos outros na seguinte ordem especificada. 
  
> [!NOTE]
> A seguinte descrição pode não listar todos os valores de campo suportados pelo Outlook; Portanto, quando seu código lê um stream existente, alguns sinalizadores que não estão listados aqui podem também ser encontrados. No entanto, você pode usar essa descrição criar programaticamente os valores da propriedade **PidTagFolderWebViewInfo** que o Outlook compreenderá. 
  
 _dwVersion_
  
> DWORD (4 bytes). A versão do formato da estrutura. A partir do Microsoft Office Outlook 2007, o único valor com suporte para este campo é da seguinte maneira.
    
|**Value name**|**Valor**|
|:-----|:-----|
|WEBVIEW_PERSISTENCE_VERSION  <br/> |0x00000002  <br/> |
   
 _dwType_
  
> DWORD (4 bytes). O tipo de informações da página inicial. A partir do Microsoft Office Outlook 2007, o único valor com suporte para este campo é da seguinte maneira.
    
|**Value name**|**Valor**|
|:-----|:-----|
|WEBVIEWURL  <br/> |0x00000001  <br/> |
   
 _dwFlags_
  
> DWORD (4 bytes). Uma combinação de zero ou mais sinalizadores cujos valores e significados estão listados na tabela a seguir.
    
|Sinalizador nome * * *|****Valor****|****Descrição****|
|:-----|:-----|:-----|
|WEBVIEW_FLAGS_SHOWBYDEFAULT  <br/> |0x00000001  <br/> |A caixa de seleção **Mostrar home page por padrão para esta pasta** foi verificada na guia **página inicial** da caixa de diálogo Propriedades de uma pasta.  <br/> |
   
 _dwUnused [7]_
  
> Uma matriz de elementos DWORD 7 (total de 28 bytes). Unused.
    
cbData diferente
  
> Um ULONG (4 bytes). O tamanho, em bytes, do elemento de dados _wzURL_ . 
    
 _wzURL_
  
> Uma matriz de elementos WCHAR. A representação UTF-16 da cadeia de caracteres de URL HomePage terminada em zero.
    
### <a name="webviewpersistenceobject-stream-sample"></a>Exemplo de fluxo de WebViewPersistenceObject

Esta seção descreve um exemplo de um fluxo de **WebViewPersistenceObject** . O fluxo Especifica a URL da home page "https://www.microsoft.com". 
  
 **Despejo de dados**
  
A seguir está um despejo do fluxo de dados como ela seria exibida em um editor de binário.
  
|**Deslocamento de fluxo**|**Bytes de dados**|**Dados ASCII**|
|:-----|:-----|:-----|
|0000000000  <br/> | `02 00 00 00 01 00 00 00 01 00 00 00 00 00 00 00` <br/> | `?...?...?.......` <br/> |
|0000000010  <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
|0000000020  <br/> | `00 00 00 00 00 00 00 00 32 00 00 00 68 00 74 00` <br/> | `........2...h.t.` <br/> |
|0000000030  <br/> | `74 00 70 00 3A 00 2F 00 2F 00 77 00 77 00 77 00` <br/> | `t.p.:././.w.w.w.` <br/> |
|0000000040  <br/> | `2E 00 6D 00 69 00 63 00 72 00 6F 00 73 00 6F 00` <br/> | `..m.i.c.r.o.s.o.` <br/> |
|0000000050  <br/> | `66 00 74 00 2E 00 63 00 6F 00 6D 00 00 00` <br/> | `f.t...c.o.m...` <br/> |
   
A seguir está uma análise dos dados de amostra para o fluxo de **WebViewPersistenceObject** . 
  
 _dwVersion_
  
> Deslocamento 0x0, 4 bytes: 0x00000002 (WEBVIEW_PERSISTENCE_VERSION).
    
 _dwType_
  
> Deslocamento 0x4, 4 bytes: 0x00000001 (WEBVIEWURL).
    
 _dwFlags_
  
> Deslocamento 0x8, 4 bytes: 0x00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT).
    
 _dwUnused [7]_
  
> Deslocamento 0xC, 28 bytes: zeros.
    
 _cbData diferente_
  
> Deslocamento 0x28, 4 bytes: 0x00000032.
    
 _wzURL_
  
> Deslocamento 0x2C, 0x32 bytes: matriz de 25 WCHARs. Um valor de cadeia de caracteres terminada em zero Unicode: "https://www.microsoft.com".
    

