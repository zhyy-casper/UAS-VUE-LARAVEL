<script setup>
import { onMounted } from 'vue';

onMounted(() => {
  Circles.create({
    id: 'circles-1',
    radius: 45,
    value: 60,
    maxValue: 100,
    width: 7,
    text: 5,
    colors: ['#f1f1f1', '#FF9E27'],
    duration: 400,
    wrpClass: 'circles-wrp',
    textClass: 'circles-text',
    styleWrapper: true,
    styleText: true
  });

  Circles.create({
    id: 'circles-2',
    radius: 45,
    value: 70,
    maxValue: 100,
    width: 7,
    text: 36,
    colors: ['#f1f1f1', '#2BB930'],
    duration: 400,
    wrpClass: 'circles-wrp',
    textClass: 'circles-text',
    styleWrapper: true,
    styleText: true
  });

  Circles.create({
    id: 'circles-3',
    radius: 45,
    value: 40,
    maxValue: 100,
    width: 7,
    text: 12,
    colors: ['#f1f1f1', '#F25961'],
    duration: 400,
    wrpClass: 'circles-wrp',
    textClass: 'circles-text',
    styleWrapper: true,
    styleText: true
  });
});
</script>

<template>
  <div class="main-panel">
    <div class="container">
      <div class="panel-header bg-primary-gradient">
        <div class="page-inner py-5">
          <div class="d-flex align-items-left align-items-md-center flex-column flex-md-row">
            <div>
              <h2 class="text-white pb-2 fw-bold">Data User</h2>
              <h5 class="text-white op-7 mb-2">
                Premium Bootstrap 4 Admin Dashboard
              </h5>
            </div>
            <div class="ml-md-auto py-2 py-md-0">
              <a href="#" class="btn btn-white btn-border btn-round mr-2">Manage</a>
              <a href="#" class="btn btn-secondary btn-round">Add Customer</a>
            </div>
          </div>
        </div>
      </div>
      <div class="page-inner mt--5">
        <div class="row mt--2">
          <div class="col-md-6">
            <div class="card full-height">
              <div class="card-body">
                <div class="card-title">Overall statistics</div>
                <div class="card-category">
                  Daily information about statistics in system
                </div>
                <div class="d-flex flex-wrap justify-content-around pb-2 pt-4">
                  <div class="px-2 pb-2 pb-md-0 text-center">
                    <div id="circles-1"></div>
                    <h6 class="fw-bold mt-3 mb-0">New Users</h6>
                  </div>
                  <div class="px-2 pb-2 pb-md-0 text-center">
                    <div id="circles-2"></div>
                    <h6 class="fw-bold mt-3 mb-0">Sales</h6>
                  </div>
                  <div class="px-2 pb-2 pb-md-0 text-center">
                    <div id="circles-3"></div>
                    <h6 class="fw-bold mt-3 mb-0">Subscribers</h6>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="col-md-6">
            <div class="card full-height">
              <div class="card-body">
                <div class="card-title">Total income & spend statistics</div>
                <div class="row py-3">
                  <div class="col-md-4 d-flex flex-column justify-content-around">
                    <div>
                      <h6 class="fw-bold text-uppercase text-success op-8">
                        Total Income
                      </h6>
                      <h3 class="fw-bold">$9.782</h3>
                    </div>
                    <div>
                      <h6 class="fw-bold text-uppercase text-danger op-8">
                        Total Spend
                      </h6>
                      <h3 class="fw-bold">$1,248</h3>
                    </div>
                  </div>
                  <div class="col-md-8">
                    <div id="chart-container">
                      <canvas id="totalIncomeChart"></canvas>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="row row-card-no-pd">
          <div class="col-md-12">
            <div class="card">
              <div class="card-header">
                <div class="card-head-row card-tools-still-right">
                  <h4 class="card-title">Users Geolocation</h4>
                  <div class="card-tools">
                    <button class="btn btn-icon btn-link btn-primary btn-xs">
                      <span class="fa fa-angle-down"></span>
                    </button>
                    <button class="btn btn-icon btn-link btn-primary btn-xs btn-refresh-card">
                      <span class="fa fa-sync-alt"></span>
                    </button>
                    <button class="btn btn-icon btn-link btn-primary btn-xs">
                      <span class="fa fa-times"></span>
                    </button>
                  </div>
                </div>
                <p class="card-category">
                  Map of the distribution of users around the world
                </p>
              </div>
              <div class="card-body">
                <div class="row">
                  <div class="col-md-6">
                    <div class="table-responsive table-hover table-sales">
                      <table class="table">
                        <tbody>
                          <tr>
                            <td>
                              <div class="flag">
                                <img src="../assets/img/flags/id.png" alt="indonesia" />
                              </div>
                            </td>
                            <td>Indonesia</td>
                            <td class="text-right">2.320</td>
                            <td class="text-right">42.18%</td>
                          </tr>
                          <tr>
                            <td>
                              <div class="flag">
                                <img src="../assets/img/flags/us.png" alt="united states" />
                              </div>
                            </td>
                            <td>USA</td>
                            <td class="text-right">240</td>
                            <td class="text-right">4.36%</td>
                          </tr>
                          <tr>
                            <td>
                              <div class="flag">
                                <img src="../assets/img/flags/au.png" alt="australia" />
                              </div>
                            </td>
                            <td>Australia</td>
                            <td class="text-right">119</td>
                            <td class="text-right">2.16%</td>
                          </tr>
                          <tr>
                            <td>
                              <div class="flag">
                                <img src="../assets/img/flags/ru.png" alt="russia" />
                              </div>
                            </td>
                            <td>Russia</td>
                            <td class="text-right">1.081</td>
                            <td class="text-right">19.65%</td>
                          </tr>
                          <tr>
                            <td>
                              <div class="flag">
                                <img src="../assets/img/flags/cn.png" alt="china" />
                              </div>
                            </td>
                            <td>China</td>
                            <td class="text-right">1.100</td>
                            <td class="text-right">20%</td>
                          </tr>
                          <tr>
                            <td>
                              <div class="flag">
                                <img src="../assets/img/flags/br.png" alt="brazil" />
                              </div>
                            </td>
                            <td>Brasil</td>
                            <td class="text-right">640</td>
                            <td class="text-right">11.63%</td>
                          </tr>
                        </tbody>
                      </table>
                    </div>
                  </div>
                  <div class="col-md-6">
                    <div class="mapcontainer">
                      <div id="map-example" class="vmap"></div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <footer class="footer">
      <div class="container-fluid">
        <nav class="pull-left">
          <ul class="nav">
            <li class="nav-item">
              <a class="nav-link" href="http://www.themekita.com/">
                ThemeKita
              </a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#"> Help </a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#"> Licenses </a>
            </li>
          </ul>
        </nav>
        <div class="copyright ml-auto">
          2018, made with <i class="fa fa-heart heart text-danger"></i> by
          <a href="http://www.themekita.com/">ThemeKita</a>
        </div>
      </div>
    </footer>
  </div>
</template>
