<template>
  <div>
    <div class="table-container">
      <table>
        <thead>
          <tr>
            <th><input id="" type="checkbox" name="" /></th>
            <th v-for="header in headers" :key="header.value">
              {{ header.text }}
            </th>
            <!-- <th>AMOUNT</th>
            <th>DESCRIPTION</th>
            <th>CUSTOMER</th>
            <th>DATE</th> -->
            <th></th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="item in items" :key="item[itemKey]">
            <td><input id="" type="checkbox" name="" /></td>
            <!-- <td>
              <span>US$352.22</span>
              <span class="table-tag">
                <span>Succeeded </span>
                <span>
                  <svg
                    width="16"
                    height="16"
                    viewBox="0 0 16 16"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <path
                      fill-rule="evenodd"
                      clip-rule="evenodd"
                      d="M5.97274 11.9097L2.21974 8.19125C1.92724 7.89575 1.92724 7.4165 2.21974 7.12175C2.51224 6.827 2.98774 6.82625 3.28024 7.12175L6.50074 10.2897L12.7167 4.09625C13.0092 3.8015 13.4847 3.8015 13.7772 4.09625C14.0697 4.391 14.0697 4.871 13.7772 5.16575L7.02499 11.906C6.88579 12.0455 6.69705 12.1241 6.50001 12.1248C6.30298 12.1255 6.11368 12.0482 5.97349 11.9097H5.97274Z"
                      fill="#0E6245"
                    />
                  </svg>
                </span>
              </span>
            </td>
            <td>fe3d8216-58f9-4dc1-aaef-2f19463b5258</td>
            <td>
              <div>hefovo87@ereyemind...</div>
            </td>
            <td>7 Jul, 14:04</td> -->
            <td v-for="dataItem in headers" :key="dataItem.value">
              <!-- {{ item[dataItem.value] }} -->
              <!-- {{ dataItem }} -->
              <!-- :data-item="item" -->
              <!-- <slot
                v-if="!$slots[dataItem.value]"
                :name="dataItem.value"

              ></slot> -->
              <slot :name="dataItem.value" :data-item="item">{{
                item[dataItem.value]
              }}</slot>
            </td>
            <td>...</td>
          </tr>
          <tr>
            <td><input id="" type="checkbox" name="" /></td>
            <td>
              <span>US$352.22</span>
              <span class="table-tag">
                <span>Succeeded </span>
                <span>
                  <svg
                    width="16"
                    height="16"
                    viewBox="0 0 16 16"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <path
                      fill-rule="evenodd"
                      clip-rule="evenodd"
                      d="M5.97274 11.9097L2.21974 8.19125C1.92724 7.89575 1.92724 7.4165 2.21974 7.12175C2.51224 6.827 2.98774 6.82625 3.28024 7.12175L6.50074 10.2897L12.7167 4.09625C13.0092 3.8015 13.4847 3.8015 13.7772 4.09625C14.0697 4.391 14.0697 4.871 13.7772 5.16575L7.02499 11.906C6.88579 12.0455 6.69705 12.1241 6.50001 12.1248C6.30298 12.1255 6.11368 12.0482 5.97349 11.9097H5.97274Z"
                      fill="#0E6245"
                    />
                  </svg>
                </span>
              </span>
            </td>
            <td>fe3d8216-58f9-4dc1-aaef-2f19463b5258</td>
            <td>
              <div>hefovo87@ereyemind...</div>
            </td>
            <td>7 Jul, 14:04</td>
            <td>...</td>
          </tr>
          <tr>
            <td><input id="" type="checkbox" name="" /></td>
            <td>
              <span>US$352.22</span>
              <span class="table-tag">
                <span>Succeeded </span>
                <span>
                  <svg
                    width="16"
                    height="16"
                    viewBox="0 0 16 16"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <path
                      fill-rule="evenodd"
                      clip-rule="evenodd"
                      d="M5.97274 11.9097L2.21974 8.19125C1.92724 7.89575 1.92724 7.4165 2.21974 7.12175C2.51224 6.827 2.98774 6.82625 3.28024 7.12175L6.50074 10.2897L12.7167 4.09625C13.0092 3.8015 13.4847 3.8015 13.7772 4.09625C14.0697 4.391 14.0697 4.871 13.7772 5.16575L7.02499 11.906C6.88579 12.0455 6.69705 12.1241 6.50001 12.1248C6.30298 12.1255 6.11368 12.0482 5.97349 11.9097H5.97274Z"
                      fill="#0E6245"
                    />
                  </svg>
                </span>
              </span>
            </td>
            <td>fe3d8216-58f9-4dc1-aaef-2f19463b5258</td>
            <td>
              <div>hefovo87@ereyemind...</div>
            </td>
            <td>7 Jul, 14:04</td>
            <td>...</td>
          </tr>
          <tr>
            <td><input id="" type="checkbox" name="" /></td>
            <td>
              <span>US$352.22</span>
              <span class="table-tag">
                <span>Succeeded </span>
                <span>
                  <svg
                    width="16"
                    height="16"
                    viewBox="0 0 16 16"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <path
                      fill-rule="evenodd"
                      clip-rule="evenodd"
                      d="M5.97274 11.9097L2.21974 8.19125C1.92724 7.89575 1.92724 7.4165 2.21974 7.12175C2.51224 6.827 2.98774 6.82625 3.28024 7.12175L6.50074 10.2897L12.7167 4.09625C13.0092 3.8015 13.4847 3.8015 13.7772 4.09625C14.0697 4.391 14.0697 4.871 13.7772 5.16575L7.02499 11.906C6.88579 12.0455 6.69705 12.1241 6.50001 12.1248C6.30298 12.1255 6.11368 12.0482 5.97349 11.9097H5.97274Z"
                      fill="#0E6245"
                    />
                  </svg>
                </span>
              </span>
            </td>
            <td>fe3d8216-58f9-4dc1-aaef-2f19463b5258</td>
            <td>
              <div>hefovo87@ereyemind...</div>
            </td>
            <td>7 Jul, 14:04</td>
            <td>...</td>
          </tr>
          <tr>
            <td><input id="" type="checkbox" name="" /></td>
            <td>
              <span>US$352.22</span>
              <span class="table-tag">
                <span>Succeeded </span>
                <span>
                  <svg
                    width="16"
                    height="16"
                    viewBox="0 0 16 16"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <path
                      fill-rule="evenodd"
                      clip-rule="evenodd"
                      d="M5.97274 11.9097L2.21974 8.19125C1.92724 7.89575 1.92724 7.4165 2.21974 7.12175C2.51224 6.827 2.98774 6.82625 3.28024 7.12175L6.50074 10.2897L12.7167 4.09625C13.0092 3.8015 13.4847 3.8015 13.7772 4.09625C14.0697 4.391 14.0697 4.871 13.7772 5.16575L7.02499 11.906C6.88579 12.0455 6.69705 12.1241 6.50001 12.1248C6.30298 12.1255 6.11368 12.0482 5.97349 11.9097H5.97274Z"
                      fill="#0E6245"
                    />
                  </svg>
                </span>
              </span>
            </td>
            <td>fe3d8216-58f9-4dc1-aaef-2f19463b5258</td>
            <td>
              <div>hefovo87@ereyemind...</div>
            </td>
            <td>7 Jul, 14:04</td>
            <td>...</td>
          </tr>
          <tr>
            <td><input id="" type="checkbox" name="" /></td>
            <td>
              <span>US$352.22</span>
              <span class="table-tag">
                <span>Succeeded </span>
                <span>
                  <svg
                    width="16"
                    height="16"
                    viewBox="0 0 16 16"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <path
                      fill-rule="evenodd"
                      clip-rule="evenodd"
                      d="M5.97274 11.9097L2.21974 8.19125C1.92724 7.89575 1.92724 7.4165 2.21974 7.12175C2.51224 6.827 2.98774 6.82625 3.28024 7.12175L6.50074 10.2897L12.7167 4.09625C13.0092 3.8015 13.4847 3.8015 13.7772 4.09625C14.0697 4.391 14.0697 4.871 13.7772 5.16575L7.02499 11.906C6.88579 12.0455 6.69705 12.1241 6.50001 12.1248C6.30298 12.1255 6.11368 12.0482 5.97349 11.9097H5.97274Z"
                      fill="#0E6245"
                    />
                  </svg>
                </span>
              </span>
            </td>
            <td>fe3d8216-58f9-4dc1-aaef-2f19463b5258</td>
            <td>
              <div>hefovo87@ereyemind...</div>
            </td>
            <td>7 Jul, 14:04</td>
            <td>...</td>
          </tr>
          <tr>
            <td><input id="" type="checkbox" name="" /></td>
            <td>
              <span>US$352.22</span>
              <span class="table-tag">
                <span>Succeeded </span>
                <span>
                  <svg
                    width="16"
                    height="16"
                    viewBox="0 0 16 16"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <path
                      fill-rule="evenodd"
                      clip-rule="evenodd"
                      d="M5.97274 11.9097L2.21974 8.19125C1.92724 7.89575 1.92724 7.4165 2.21974 7.12175C2.51224 6.827 2.98774 6.82625 3.28024 7.12175L6.50074 10.2897L12.7167 4.09625C13.0092 3.8015 13.4847 3.8015 13.7772 4.09625C14.0697 4.391 14.0697 4.871 13.7772 5.16575L7.02499 11.906C6.88579 12.0455 6.69705 12.1241 6.50001 12.1248C6.30298 12.1255 6.11368 12.0482 5.97349 11.9097H5.97274Z"
                      fill="#0E6245"
                    />
                  </svg>
                </span>
              </span>
            </td>
            <td>fe3d8216-58f9-4dc1-aaef-2f19463b5258</td>
            <td>
              <div>hefovo87@ereyemind...</div>
            </td>
            <td>7 Jul, 14:04</td>
            <td>...</td>
          </tr>
          <tr>
            <td><input id="" type="checkbox" name="" /></td>
            <td>
              <span>US$352.22</span>
              <span class="table-tag">
                <span>Succeeded </span>
                <span>
                  <svg
                    width="16"
                    height="16"
                    viewBox="0 0 16 16"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <path
                      fill-rule="evenodd"
                      clip-rule="evenodd"
                      d="M5.97274 11.9097L2.21974 8.19125C1.92724 7.89575 1.92724 7.4165 2.21974 7.12175C2.51224 6.827 2.98774 6.82625 3.28024 7.12175L6.50074 10.2897L12.7167 4.09625C13.0092 3.8015 13.4847 3.8015 13.7772 4.09625C14.0697 4.391 14.0697 4.871 13.7772 5.16575L7.02499 11.906C6.88579 12.0455 6.69705 12.1241 6.50001 12.1248C6.30298 12.1255 6.11368 12.0482 5.97349 11.9097H5.97274Z"
                      fill="#0E6245"
                    />
                  </svg>
                </span>
              </span>
            </td>
            <td>fe3d8216-58f9-4dc1-aaef-2f19463b5258</td>
            <td>
              <div>hefovo87@ereyemind...</div>
            </td>
            <td>7 Jul, 14:04</td>
            <td>...</td>
          </tr>
          <tr>
            <td><input id="" type="checkbox" name="" /></td>
            <td>
              <span>US$352.22</span>
              <span class="table-tag">
                <span>Succeeded </span>
                <span>
                  <svg
                    width="16"
                    height="16"
                    viewBox="0 0 16 16"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <path
                      fill-rule="evenodd"
                      clip-rule="evenodd"
                      d="M5.97274 11.9097L2.21974 8.19125C1.92724 7.89575 1.92724 7.4165 2.21974 7.12175C2.51224 6.827 2.98774 6.82625 3.28024 7.12175L6.50074 10.2897L12.7167 4.09625C13.0092 3.8015 13.4847 3.8015 13.7772 4.09625C14.0697 4.391 14.0697 4.871 13.7772 5.16575L7.02499 11.906C6.88579 12.0455 6.69705 12.1241 6.50001 12.1248C6.30298 12.1255 6.11368 12.0482 5.97349 11.9097H5.97274Z"
                      fill="#0E6245"
                    />
                  </svg>
                </span>
              </span>
            </td>
            <td>fe3d8216-58f9-4dc1-aaef-2f19463b5258</td>
            <td>
              <div>hefovo87@ereyemind...</div>
            </td>
            <td>7 Jul, 14:04</td>
            <td>...</td>
          </tr>
          <tr>
            <td><input id="" type="checkbox" name="" /></td>
            <td>
              <span>US$352.22</span>
              <span class="table-tag">
                <span>Succeeded </span>
                <span>
                  <svg
                    width="16"
                    height="16"
                    viewBox="0 0 16 16"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <path
                      fill-rule="evenodd"
                      clip-rule="evenodd"
                      d="M5.97274 11.9097L2.21974 8.19125C1.92724 7.89575 1.92724 7.4165 2.21974 7.12175C2.51224 6.827 2.98774 6.82625 3.28024 7.12175L6.50074 10.2897L12.7167 4.09625C13.0092 3.8015 13.4847 3.8015 13.7772 4.09625C14.0697 4.391 14.0697 4.871 13.7772 5.16575L7.02499 11.906C6.88579 12.0455 6.69705 12.1241 6.50001 12.1248C6.30298 12.1255 6.11368 12.0482 5.97349 11.9097H5.97274Z"
                      fill="#0E6245"
                    />
                  </svg>
                </span>
              </span>
            </td>
            <td>fe3d8216-58f9-4dc1-aaef-2f19463b5258</td>
            <td>
              <div>hefovo87@ereyemind...</div>
            </td>
            <td>7 Jul, 14:04</td>
            <td>...</td>
          </tr>
          <tr>
            <td><input id="" type="checkbox" name="" /></td>
            <td>
              <span>US$352.22</span>
              <span class="table-tag">
                <span>Succeeded </span>
                <span>
                  <svg
                    width="16"
                    height="16"
                    viewBox="0 0 16 16"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <path
                      fill-rule="evenodd"
                      clip-rule="evenodd"
                      d="M5.97274 11.9097L2.21974 8.19125C1.92724 7.89575 1.92724 7.4165 2.21974 7.12175C2.51224 6.827 2.98774 6.82625 3.28024 7.12175L6.50074 10.2897L12.7167 4.09625C13.0092 3.8015 13.4847 3.8015 13.7772 4.09625C14.0697 4.391 14.0697 4.871 13.7772 5.16575L7.02499 11.906C6.88579 12.0455 6.69705 12.1241 6.50001 12.1248C6.30298 12.1255 6.11368 12.0482 5.97349 11.9097H5.97274Z"
                      fill="#0E6245"
                    />
                  </svg>
                </span>
              </span>
            </td>
            <td>fe3d8216-58f9-4dc1-aaef-2f19463b5258</td>
            <td>
              <div>hefovo87@ereyemind...</div>
            </td>
            <td>7 Jul, 14:04</td>
            <td>...</td>
          </tr>
          <tr>
            <td><input id="" type="checkbox" name="" /></td>
            <td>
              <span>US$352.22</span>
              <span class="table-tag">
                <span>Succeeded </span>
                <span>
                  <svg
                    width="16"
                    height="16"
                    viewBox="0 0 16 16"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <path
                      fill-rule="evenodd"
                      clip-rule="evenodd"
                      d="M5.97274 11.9097L2.21974 8.19125C1.92724 7.89575 1.92724 7.4165 2.21974 7.12175C2.51224 6.827 2.98774 6.82625 3.28024 7.12175L6.50074 10.2897L12.7167 4.09625C13.0092 3.8015 13.4847 3.8015 13.7772 4.09625C14.0697 4.391 14.0697 4.871 13.7772 5.16575L7.02499 11.906C6.88579 12.0455 6.69705 12.1241 6.50001 12.1248C6.30298 12.1255 6.11368 12.0482 5.97349 11.9097H5.97274Z"
                      fill="#0E6245"
                    />
                  </svg>
                </span>
              </span>
            </td>
            <td>fe3d8216-58f9-4dc1-aaef-2f19463b5258</td>
            <td>
              <div>hefovo87@ereyemind...</div>
            </td>
            <td>7 Jul, 14:04</td>
            <td>...</td>
          </tr>
          <tr>
            <td><input id="" type="checkbox" name="" /></td>
            <td>
              <span>US$352.22</span>
              <span class="table-tag">
                <span>Succeeded </span>
                <span>
                  <svg
                    width="16"
                    height="16"
                    viewBox="0 0 16 16"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <path
                      fill-rule="evenodd"
                      clip-rule="evenodd"
                      d="M5.97274 11.9097L2.21974 8.19125C1.92724 7.89575 1.92724 7.4165 2.21974 7.12175C2.51224 6.827 2.98774 6.82625 3.28024 7.12175L6.50074 10.2897L12.7167 4.09625C13.0092 3.8015 13.4847 3.8015 13.7772 4.09625C14.0697 4.391 14.0697 4.871 13.7772 5.16575L7.02499 11.906C6.88579 12.0455 6.69705 12.1241 6.50001 12.1248C6.30298 12.1255 6.11368 12.0482 5.97349 11.9097H5.97274Z"
                      fill="#0E6245"
                    />
                  </svg>
                </span>
              </span>
            </td>
            <td>fe3d8216-58f9-4dc1-aaef-2f19463b5258</td>
            <td>
              <div>hefovo87@ereyemind...</div>
            </td>
            <td>7 Jul, 14:04</td>
            <td>...</td>
          </tr>
          <tr>
            <td><input id="" type="checkbox" name="" /></td>
            <td>
              <span>US$352.22</span>
              <span class="table-tag">
                <span>Succeeded </span>
                <span>
                  <svg
                    width="16"
                    height="16"
                    viewBox="0 0 16 16"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <path
                      fill-rule="evenodd"
                      clip-rule="evenodd"
                      d="M5.97274 11.9097L2.21974 8.19125C1.92724 7.89575 1.92724 7.4165 2.21974 7.12175C2.51224 6.827 2.98774 6.82625 3.28024 7.12175L6.50074 10.2897L12.7167 4.09625C13.0092 3.8015 13.4847 3.8015 13.7772 4.09625C14.0697 4.391 14.0697 4.871 13.7772 5.16575L7.02499 11.906C6.88579 12.0455 6.69705 12.1241 6.50001 12.1248C6.30298 12.1255 6.11368 12.0482 5.97349 11.9097H5.97274Z"
                      fill="#0E6245"
                    />
                  </svg>
                </span>
              </span>
            </td>
            <td>fe3d8216-58f9-4dc1-aaef-2f19463b5258</td>
            <td>
              <div>hefovo87@ereyemind...</div>
            </td>
            <td>7 Jul, 14:04</td>
            <td>...</td>
          </tr>
          <tr>
            <td><input id="" type="checkbox" name="" /></td>
            <td>
              <span>US$352.22</span>
              <span class="table-tag">
                <span>Succeeded </span>
                <span>
                  <svg
                    width="16"
                    height="16"
                    viewBox="0 0 16 16"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <path
                      fill-rule="evenodd"
                      clip-rule="evenodd"
                      d="M5.97274 11.9097L2.21974 8.19125C1.92724 7.89575 1.92724 7.4165 2.21974 7.12175C2.51224 6.827 2.98774 6.82625 3.28024 7.12175L6.50074 10.2897L12.7167 4.09625C13.0092 3.8015 13.4847 3.8015 13.7772 4.09625C14.0697 4.391 14.0697 4.871 13.7772 5.16575L7.02499 11.906C6.88579 12.0455 6.69705 12.1241 6.50001 12.1248C6.30298 12.1255 6.11368 12.0482 5.97349 11.9097H5.97274Z"
                      fill="#0E6245"
                    />
                  </svg>
                </span>
              </span>
            </td>
            <td>fe3d8216-58f9-4dc1-aaef-2f19463b5258</td>
            <td>
              <div>hefovo87@ereyemind...</div>
            </td>
            <td>7 Jul, 14:04</td>
            <td>...</td>
          </tr>
          <tr>
            <td><input id="" type="checkbox" name="" /></td>
            <td>
              <span>US$352.22</span>
              <span class="table-tag">
                <span>Succeeded </span>
                <span>
                  <svg
                    width="16"
                    height="16"
                    viewBox="0 0 16 16"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <path
                      fill-rule="evenodd"
                      clip-rule="evenodd"
                      d="M5.97274 11.9097L2.21974 8.19125C1.92724 7.89575 1.92724 7.4165 2.21974 7.12175C2.51224 6.827 2.98774 6.82625 3.28024 7.12175L6.50074 10.2897L12.7167 4.09625C13.0092 3.8015 13.4847 3.8015 13.7772 4.09625C14.0697 4.391 14.0697 4.871 13.7772 5.16575L7.02499 11.906C6.88579 12.0455 6.69705 12.1241 6.50001 12.1248C6.30298 12.1255 6.11368 12.0482 5.97349 11.9097H5.97274Z"
                      fill="#0E6245"
                    />
                  </svg>
                </span>
              </span>
            </td>
            <td>fe3d8216-58f9-4dc1-aaef-2f19463b5258</td>
            <td>
              <div>hefovo87@ereyemind...</div>
            </td>
            <td>7 Jul, 14:04</td>
            <td>...</td>
          </tr>
          <tr>
            <td><input id="" type="checkbox" name="" /></td>
            <td>
              <span>US$352.22</span>
              <span class="table-tag">
                <span>Succeeded </span>
                <span>
                  <svg
                    width="16"
                    height="16"
                    viewBox="0 0 16 16"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <path
                      fill-rule="evenodd"
                      clip-rule="evenodd"
                      d="M5.97274 11.9097L2.21974 8.19125C1.92724 7.89575 1.92724 7.4165 2.21974 7.12175C2.51224 6.827 2.98774 6.82625 3.28024 7.12175L6.50074 10.2897L12.7167 4.09625C13.0092 3.8015 13.4847 3.8015 13.7772 4.09625C14.0697 4.391 14.0697 4.871 13.7772 5.16575L7.02499 11.906C6.88579 12.0455 6.69705 12.1241 6.50001 12.1248C6.30298 12.1255 6.11368 12.0482 5.97349 11.9097H5.97274Z"
                      fill="#0E6245"
                    />
                  </svg>
                </span>
              </span>
            </td>
            <td>fe3d8216-58f9-4dc1-aaef-2f19463b5258</td>
            <td>
              <div>hefovo87@ereyemind...</div>
            </td>
            <td>7 Jul, 14:04</td>
            <td>...</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="d-flex table-footer justify-content-between">
      <span>{{ items.length }} results</span>
      <div>
        <button class="button btn-disabled">Previous</button>
        <Button> Next </Button>
      </div>
    </div>
  </div>
</template>

<script>
import Button from './Button.vue'
export default {
  components: { Button },
  props: {
    headers: {
      type: Array,
      default: () => {
        return []
      },
    },
    items: {
      type: Array,
      default: () => {
        return []
      },
    },
    itemKey: {
      type: String,
      default: () => {
        return ''
      },
    },
  },
  created() {
    console.log(this.$slots, this.$scopedSlots)
  },
}
</script>
