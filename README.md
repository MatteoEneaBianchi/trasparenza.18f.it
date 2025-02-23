# trasparenza.18f.it



{% for atto in site.data.trasparenza %}
<div class="col-12 amministrazione amministrazione-primary">
    <div class="row">
        <div class="col-md-4 fw-bold">Tipologia dell'atto:</div>
        <div class="col-md-8">{{ atto.tipologia }}</div>
    </div>
    <div class="row">
        <div class="col-md-4 fw-bold">Ufficio:</div>
        <div class="col-md-8">{{ atto.ufficio }}</div>
    </div>
    <div class="row">
        <div class="col-md-4 fw-bold">Oggetto:</div>
        <div class="col-md-8">{{ atto.oggetto }}</div>
    </div>
    <div class="row">
        <div class="col-md-4 fw-bold">Periodo di pubblicazione:</div>
        <div class="col-md-8">{{ atto.pubblicazione }}</div>
    </div>
    <div class="row">
        <div class="col-md-4 fw-bold">Numero atto:</div>
        <div class="col-md-8">{{ atto.numero }}</div>
    </div>
    <div class="row">
        <div class="col-md-4 fw-bold">Allegati:</div>
        <div class="col-md-8 overflow-hidden">
            {% for allegato in atto.allegati %}
                <div>
                    <a target="_blank" href="{{ allegato.link }}">{{ allegato.nome }}</a>
                </div>
            {% endfor %}
        </div>
    </div>
</div>
{% endfor %}



