<div align="center">
  <h1 style="font-size: 70px; font-weight: bold;">
  ✮ ═══  ᗯEᗷ ᑕOᑎᑕIEᑎᑕIᗩ ᗩᗰᗷIEᑎTᗩᒪ  ═══ ✮
  </h1>

  <img src="https://i.pinimg.com/1200x/4c/d6/3c/4cd63c93075047a6c1395d6b1e287253.jpg" width="600" alt="GIF Banner">
</div>


-----------------------------------
ʙᴀꜱᴇ.ʜᴛᴍʟ
-----------------------------------
```html
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>Conciencia Ambiental</title>
<!-- Bootstrap 5 -->
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css"
rel="stylesheet">
<!-- Estilos personalizados -->
<link href="{{ url_for('static', filename='css/style.css') }}" rel="stylesheet">
</head>
<body>
<!-- NAVBAR -->
<nav class="navbar navbar-expand-lg navbar-dark bg-success">
<div class="container">
    <a class="navbar-brand" href="{{ url_for('index') }}"> Medio Ambiente</a>

    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-
    target="#menu">
        <span class="navbar-toggler-icon"></span>
    </button>

    <div class="collapse navbar-collapse" id="menu">
        <ul class="navbar-nav ms-auto">
            <li class="nav-item"><a class="nav-link" href="{{ url_for('index') }}">Inicio</a></li>
            <li class="nav-item"><a class="nav-link" href="{{ url_for('sistema') }}">Sistema Ambiental</a></li>
            <li class="nav-item"><a class="nav-link" href="{{ url_for('futuro') }}">Futuro</a></li>
            <li class="nav-item"><a class="nav-link" href="{{ url_for('tres_r') }}">3 R</a></li>
        </ul>
    </div>
</div>
</nav>

<!-- BREADCRUMB -->
<div class="container mt-3">
<nav>
<ol class="breadcrumb">
{% for item in breadcrumb %}
<li class="breadcrumb-item">{{ item }}</li>
{% endfor %}
</ol>
</nav>
</div>

<!-- CONTENIDO -->
<div class="container mt-4">
{% block content %}{% endblock %}
</div>

<footer class="bg-dark text-white text-center p-3 mt-5">
Cuidar el planeta es responsabilidad de todos
</footer>

<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

-----------------------------------
ꜰᴜᴛᴜʀᴏ.ʜᴛᴍʟ
-----------------------------------

``` html
{% extends "base.html" %}
{% block content %}
<div class="fade-in">
    <div class="page-header">
        <h2 class="mb-3">El planeta que dejaremos a nuestros hijos</h2>
        <div class="environment-icon">🌍</div>
    </div>

    <div class="row">
        <div class="col-md-6">
            <img src="{{ url_for('static', filename='images/futuro.jpg') }}"
                 class="img-fluid rounded mb-4 shadow-soft"
                 alt="Futuro del planeta">
        </div>
        <div class="col-md-6">
            <div class="card shadow-soft">
                <div class="card-body">
                    <p class="lead">
                        Las decisiones que tomamos hoy impactarán directamente
                        la calidad de vida de las próximas generaciones.
                    </p>
                    <p>
                        Es nuestra responsabilidad colectiva construir un futuro sostenible
                        donde nuestros hijos puedan disfrutar de un planeta saludable y próspero.
                    </p>
                    <div class="alert alert-warning" role="alert">
                        <strong>¡Actúa ahora!</strong> Cada acción cuenta para preservar nuestro hogar.
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>
{% endblock %}

```
-----------------------------------
INDEX.HTML
-----------------------------------
``` html
{% extends "base.html" %}
{% block content %}
<div class="fade-in">
    <div class="row align-items-center">
        <div class="col-md-6">
            <h1 class="mb-4">¿Por qué es importante cuidar el medio ambiente?</h1>
            <p class="lead mb-4">
                El medio ambiente es la base de la vida. Protegerlo garantiza bienestar,
                salud y recursos para las futuras generaciones.
            </p>
            <div class="d-flex gap-3">
                <a href="{{ url_for('sistema') }}" class="btn btn-primary btn-lg">Sistema Ambiental</a>
                <a href="{{ url_for('futuro') }}" class="btn btn-outline-primary btn-lg">Futuro del Planeta</a>
            </div>
        </div>
        <div class="col-md-6">
            <img src="{{ url_for('static', filename='images/ambiente.jpg') }}"
                 class="img-fluid rounded shadow-soft"
                 alt="Cuidado del medio ambiente">
        </div>
    </div>

    <div class="row mt-5">
        <div class="col-md-4">
            <div class="card text-center h-100 shadow-soft">
                <div class="card-body">
                    <div class="environment-icon">🌍</div>
                    <h5 class="card-title">Planeta Saludable</h5>
                    <p class="card-text">Preservar los recursos naturales para un futuro sostenible.</p>
                </div>
            </div>
        </div>
        <div class="col-md-4">
            <div class="card text-center h-100 shadow-soft">
                <div class="card-body">
                    <div class="environment-icon">♻️</div>
                    <h5 class="card-title">Reciclaje</h5>
                    <p class="card-text">Reducir, reutilizar y reciclar para minimizar residuos.</p>
                </div>
            </div>
        </div>
        <div class="col-md-4">
            <div class="card text-center h-100 shadow-soft">
                <div class="card-body">
                    <div class="environment-icon">🌱</div>
                    <h5 class="card-title">Conservación</h5>
                    <p class="card-text">Proteger la biodiversidad y los ecosistemas naturales.</p>
                </div>
            </div>
        </div>
    </div>
</div>
{% endblock %}


```

-----------------------------------
ꜱɪꜱᴛᴇᴍᴀ.ʜᴛᴍʟ
-----------------------------------
``` html
{% extends "base.html" %}
{% block content %}
<div class="fade-in">
    <div class="page-header">
        <h2 class="mb-3">Sistema de Gestión Ambiental</h2>
        <div class="environment-icon">🌱</div>
    </div>

    <div class="row">
        <div class="col-md-6">
            <img src="{{ url_for('static', filename='images/sistema.jpg') }}"
                 class="img-fluid rounded mb-4 shadow-soft"
                 alt="Sistema de Gestión Ambiental">
        </div>
        <div class="col-md-6">
            <div class="card shadow-soft">
                <div class="card-body">
                    <p class="lead">
                        Un Sistema de Gestión Ambiental (SGA) es un conjunto de políticas,
                        procedimientos y prácticas que permiten a organizaciones reducir
                        su impacto ambiental y cumplir con normativas ecológicas.
                    </p>
                    <p>
                        Los SGA ayudan a las empresas a ser más sostenibles y responsables
                        con el medio ambiente, contribuyendo así a la preservación del planeta.
                    </p>
                </div>
            </div>
        </div>
    </div>
</div>
{% endblock %}
```

-----------------------------------
ᴛʀᴇꜱ_ʀ.ʜᴛᴍʟ
-----------------------------------
``` html
{% extends "base.html" %}
{% block content %}
<div class="fade-in">
    <div class="page-header">
        <h2 class="mb-4">Las 3 R del cuidado ambiental</h2>
        <div class="environment-icon">♻️</div>
    </div>

    <div class="row mb-5">
        <div class="col-md-4">
            <div class="card text-center h-100 shadow-soft">
                <div class="card-header bg-primary text-white">
                    <h4 class="mb-0">Reducir</h4>
                </div>
                <div class="card-body">
                    <div class="environment-icon">📉</div>
                    <p class="card-text">Consumir solo lo necesario para minimizar el impacto ambiental.</p>
                </div>
            </div>
        </div>
        <div class="col-md-4">
            <div class="card text-center h-100 shadow-soft">
                <div class="card-header bg-success text-white">
                    <h4 class="mb-0">Reutilizar</h4>
                </div>
                <div class="card-body">
                    <div class="environment-icon">🔄</div>
                    <p class="card-text">Dar una segunda vida a los objetos antes de desecharlos.</p>
                </div>
            </div>
        </div>
        <div class="col-md-4">
            <div class="card text-center h-100 shadow-soft">
                <div class="card-header bg-info text-white">
                    <h4 class="mb-0">Reciclar</h4>
                </div>
                <div class="card-body">
                    <div class="environment-icon">♻️</div>
                    <p class="card-text">Transformar residuos en nuevos productos útiles.</p>
                </div>
            </div>
        </div>
    </div>

    <div class="text-center">
        <img src="{{ url_for('static', filename='images/reciclaje.jpg') }}"
             class="img-fluid rounded shadow-soft"
             alt="Reciclaje y las 3R">
    </div>
</div>
{% endblock %}
```
