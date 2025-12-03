<%@ page language="java" contentType="text/html; charset=UTF-8" pageEncoding="UTF-8" isELIgnored="false"%>
<!DOCTYPE html>
<%@ page import="java.util.*" %>
<%@ taglib uri="http://java.sun.com/jstl/core_rt" prefix="c" %>
<%@ taglib prefix="snk" uri="/WEB-INF/tld/sankhyaUtil.tld" %>
<%@ taglib uri="http://java.sun.com/jsp/jstl/fmt" prefix="fmt" %>
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Card — Status de Pedidos</title>
  <style>
    :root{
      --bg: #0f172a;
      --card: #0b1220;
      --muted: #9aa4b2;
      --glass: rgba(255,255,255,0.03);
      --accent: linear-gradient(90deg,#6ee7b7,#3b82f6);
      --success: #10b981;
      --danger: #ef4444;
      --warning: #f59e0b;
      --info: #3b82f6;
      --surface: #071028;
    }
    *{box-sizing:border-box}
    body{
      margin:0;
      min-height:100vh;
      display:flex;
      align-items:center;
      justify-content:center;
      background: transparent !important;
      font-family: Inter, ui-sans-serif, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
      color:#e6eef8;
      padding:24px;
    }

    .card{
      width:100%;
      max-width:980px;
      background: rgba(30, 46, 82, 0.945);
      border:1px solid rgba(255,255,255,0.04);
      border-radius:14px;
      padding:18px;
      box-shadow: 0 6px 30px rgba(2,6,23,0.6);
      backdrop-filter: blur(6px);
    }

    .card-header{
      display:flex;
      gap:12px;
      align-items:center;
      justify-content:space-between;
      margin-bottom:12px;
    }
    .title{
      display:flex;
      gap:12px;
      align-items:center;
    }
    .logo{
      width:48px;height:48px;border-radius:10px;
      background:var(--glass);display:flex;align-items:center;justify-content:center;font-weight:700;color:#dbeafe;font-size:18px
    }
    h1{font-size:18px;margin:0}
    p.sub{margin:0;color:var(--muted);font-size:13px}

    .controls{display:flex;gap:8px;align-items:center}
    .btn{
      background:transparent;border:1px solid rgba(255,255,255,0.04);color:var(--muted);padding:8px 10px;border-radius:8px;font-size:13px
    }
    .btn.primary{background:linear-gradient(90deg,#2563eb,#06b6d4);color:white;border:0}

    .grid{
      display:grid;
      grid-template-columns: repeat(3,1fr);
      gap:12px;
      cursor: pointer;
    }
    @media (max-width:820px){.grid{grid-template-columns:repeat(2,1fr)}}
    @media (max-width:520px){.grid{grid-template-columns:1fr}}

    .status-card{
      background: linear-gradient(180deg, rgba(255,255,255,0.015), rgba(255,255,255,0.01));
      border:1px solid rgba(255,255,255,0.025);
      padding:12px;border-radius:10px;display:flex;gap:12px;align-items:center;
    }
    .status-icon{width:56px;height:56px;border-radius:8px;display:flex;align-items:center;justify-content:center;font-weight:700;font-size:18px}
    .status-info{flex:1}
    .status-label{font-size:14px;margin:0 0 6px 0}
    .status-count{font-size:20px;font-weight:700;margin:0;color:#fff}
    .status-meta{font-size:12px;color:var(--muted);margin-top:6px}

    /* color variants */
    .c-progress{background: linear-gradient(180deg, rgba(59,130,246,0.14), rgba(59,130,246,0.06)); border-left:4px solid rgba(59,130,246,0.9)}
    .c-await{background: linear-gradient(180deg, rgba(245,158,11,0.08), rgba(245,158,11,0.03)); border-left:4px solid rgba(245,158,11,0.9)}
    .c-ok{background: linear-gradient(180deg, rgba(16,185,129,0.08), rgba(16,185,129,0.03)); border-left:4px solid rgba(16,185,129,0.9)}
    .c-warn{background: linear-gradient(180deg, rgba(239,68,68,0.06), rgba(239,68,68,0.02)); border-left:4px solid rgba(239,68,68,0.9)}
    .c-neutral{background: linear-gradient(180deg, rgba(148,163,184,0.03), rgba(148,163,184,0.01)); border-left:4px solid rgba(148,163,184,0.5)}

    .legend{display:flex;gap:8px;flex-wrap:wrap;margin-top:12px}
    .chip{font-size:13px;padding:6px 8px;border-radius:999px;background:rgba(255,255,255,0.02);color:var(--muted);border:1px solid rgba(255,255,255,0.02)}

    .small{font-size:12px;color:var(--muted)}
  </style>
  <snk:load/>
</head>
<body>
  <div class="card" role="region" aria-label="Painel de status de pedidos">
    <div class="card-header">
      <div class="title">
        <div class="logo">LJ</div>
        <div>
          <h1>Pedidos Status geral</h1>
          <p class="sub">Visão rápida dos status mais importantes - Gestor</p>
        </div>
      </div>

      <!--<div class="controls">
        <button class="btn">⟳ Atualizar</button>
        <button class="btn primary">Demo</button>
      </div>-->
    </div>
    <snk:query var="pedidos">
        SELECT
            COUNT(DISTINCT CASE WHEN SNK_GET_SATUSCONFERENCIA(CAB.NUNOTA) IN ('AC') THEN CAB.NUNOTA END) AS AGUARDANDO_CONFERENCIA,
            COUNT(DISTINCT CASE WHEN SNK_GET_SATUSCONFERENCIA(CAB.NUNOTA) IN ('Z', 'RZ') THEN CAB.NUNOTA END) AS AGUARDANDO_FINALIZACAO,
            COUNT(DISTINCT CASE WHEN SNK_GET_SATUSCONFERENCIA(CAB.NUNOTA) = 'C'  THEN CAB.NUNOTA END) AS AGUARDANDO_LIB_CORTE,
            COUNT(DISTINCT CASE WHEN SNK_GET_SATUSCONFERENCIA(CAB.NUNOTA) IN ('AL') THEN CAB.NUNOTA END) AS AGUARDANDO_LIB_CONF,
            COUNT(DISTINCT CASE WHEN SNK_GET_SATUSCONFERENCIA(CAB.NUNOTA) IN ('A','RA')  THEN CAB.NUNOTA END) AS EM_ANDAMENTO,
            COUNT(DISTINCT CASE WHEN SNK_GET_SATUSCONFERENCIA(CAB.NUNOTA) IN ('D','RD')  THEN CAB.NUNOTA END) AS FINALIZADA_DIVERGENTE,
            COUNT(DISTINCT CASE WHEN SNK_GET_SATUSCONFERENCIA(CAB.NUNOTA) IN ('F') THEN CAB.NUNOTA END) AS FINALIZADA_OK,
            COUNT(DISTINCT CASE WHEN SNK_GET_SATUSCONFERENCIA(CAB.NUNOTA) = 'RA' THEN CAB.NUNOTA END) AS RECONTAGEM_ANDAMENTO,
            COUNT(DISTINCT CASE WHEN SNK_GET_SATUSCONFERENCIA(CAB.NUNOTA) = 'R'  THEN CAB.NUNOTA END) AS AGUARDANDO_RECONTAGEM,
            COUNT(DISTINCT CASE WHEN SNK_GET_SATUSCONFERENCIA(CAB.NUNOTA) = 'RD' THEN CAB.NUNOTA END) AS RECONTAGEM_DIVERGENTE,
            COUNT(DISTINCT CASE WHEN SNK_GET_SATUSCONFERENCIA(CAB.NUNOTA) = 'RF' THEN CAB.NUNOTA END) AS RECONTAGEM_OK,
            COUNT(DISTINCT CASE 
                    WHEN CTR.DHINI IS NOT NULL 
                    AND CTR.DHFIN IS NULL 
                    THEN CAB.NUNOTA 
                END) AS EM_SEPARACAO

        FROM TGFCAB CAB
        LEFT JOIN AD_CTRLSEPEST CTR ON CTR.NUNOTA = CAB.NUNOTA
        WHERE CAB.DTNEG BETWEEN TRUNC(SYSDATE, 'MM') AND SYSDATE
        AND CAB.TIPMOV = 'P'


    </snk:query>
    <c:forEach var="row" items="${pedidos.rows}" varStatus="status">
    <div class="grid" onclick="openApp('br.com.sankhya.menu.adicional.nuDsb.197.1',{});">
       <div class="status-card c-await">
        <div class="status-icon">+</div>
        <div class="status-info">
          <p class="status-label">Aguardando liberação p/ conferência</p>
          <p class="status-count"><c:out value="${row.AGUARDANDO_LIB_CONF}"/></p>
        </div>
      </div> 
        <div class="status-card c-progress">
        <div class="status-icon">+</div>
        <div class="status-info">
          <p class="status-label">Em separação</p>
          <p class="status-count"><c:out value="${row.EM_SEPARACAO}"/></p>
        </div>
      </div>
      <div class="status-card c-await">
        <div class="status-icon">+</div>
        <div class="status-info">
          <p class="status-label">Aguardando conferência</p>
          <p class="status-count"><c:out value="${row.AGUARDANDO_CONFERENCIA}"/></p>
        </div>
      </div>
      <div class="status-card c-progress">
        <div class="status-icon">+</div>
        <div class="status-info">
          <p class="status-label">Em andamento</p>
          <p class="status-count"><c:out value="${row.EM_ANDAMENTO}"/></p>
        </div>
      </div>
      <div class="status-card c-warn">
        <div class="status-icon">+</div>
        <div class="status-info">
          <p class="status-label">Aguardando liberação de corte</p>
          <p class="status-count"><c:out value="${row.AGUARDANDO_LIB_CORTE}"/></p>
        </div>
      </div>

      <div class="status-card c-warn">
        <div class="status-icon">+</div>
        <div class="status-info">
          <p class="status-label">Finalizada divergente</p>
          <p class="status-count"><c:out value="${row.FINALIZADA_DIVERGENTE}"/></p>
        </div>
      </div>

      <div class="status-card c-neutral">
        <div class="status-icon">+</div>
        <div class="status-info">
          <p class="status-label">Aguardando finalização</p>
          <p class="status-count"><c:out value="${row.AGUARDANDO_FINALIZACAO}"/></p>
        </div>
      </div>

      <div class="status-card c-await">
        <div class="status-icon">+</div>
        <div class="status-info">
          <p class="status-label">Aguardando recontagem</p>
          <p class="status-count"><c:out value="${row.AGUARDANDO_RECONTAGEM}"/></p>
        </div>
      </div>

      <div class="status-card c-progress">
        <div class="status-icon">+</div>
        <div class="status-info">
          <p class="status-label">Recontagem em andamento</p>
          <p class="status-count"><c:out value="${row.RECONTAGEM_ANDAMENTO}"/></p>
        </div>
      </div>

      <div class="status-card c-warn">
        <div class="status-icon">+</div>
        <div class="status-info">
          <p class="status-label">Recontagem finalizada divergente</p>
          <p class="status-count"><c:out value="${row.RECONTAGEM_DIVERGENTE}"/></p>
        </div>
      </div>
      <div class="status-card c-ok">
        <div class="status-icon">+</div>
        <div class="status-info">
          <p class="status-label">Finalizado OK</p>
          <p class="status-count"><c:out value="${row.FINALIZADA_OK}"/></p>
        </div>
      </div>
      <div class="status-card c-ok">
        <div class="status-icon">+</div>
        <div class="status-info">
          <p class="status-label">Recontagem OK</p>
          <p class="status-count"><c:out value="${row.RECONTAGEM_OK}"/></p>
        </div>
      </div>
      </c:forEach>